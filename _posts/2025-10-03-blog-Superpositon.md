---
title: 'Superposition in Neural Networks: Tackling the Challenge of Polysemantic Neurons'
date: 2025-10-03
permalink: /posts/blog/superposition
---

This blog summarizes the superposition problem, with the aim of addressing the issue that a single neuron or attention head may simultaneously represent multiple concepts.

<!-- excerpt -->

### 问题描述
在openai的blog当中，研究通过对 GPT-2 XL 等模型的神经元分析发现，多数神经元表现出显著的多义性。即单个神经元并非只对某一类单一语义模式（如 “漫威电影相关词汇”“过去时态动词”）激活，而是同时对多个无关或弱相关的语义概念产生响应。

现有解释方法（如基于 GPT-4 的自然语言解释）难以捕捉复杂的多义性。若神经元同时对应多个概念，解释往往只能覆盖其中一个或部分核心概念，导致 “解释不完整”。为兼顾多个概念，解释可能变得过度宽泛（如将 “既对‘not all’激活，也对‘部分否定短语’激活” 简化为 “对否定相关词汇激活”），反而降低解释的精准度。

对于多义性的成因，研究人员从以下几个角度进行了阐述。首先是**叠加效应（Superposition）**。研究认为，多义性可能源于模型为高效利用参数而采用的 “叠加表示”—— 即多个语义特征被压缩到同一组神经元中，而非分配到独立神经元。这种机制在参数受限的模型中更明显：为在有限神经元数量下编码足够多的语义信息，模型被迫让单个神经元承担多语义角色，尤其在深层模型（如 GPT-3 系列大模型）中，叠加效应更显著，导致多义性比例升高。其次，实验发现，使用**稀疏激活函数**（如 ReLU，或设置低激活密度如 0.01）的模型，多义性程度低于使用 GELU 等稠密激活函数的模型。原因是稀疏激活强制神经元 “专注于少数模式”，减少了单神经元对多语义的响应。**模型规模扩大**时，多义性问题加剧：对 GPT-3 系列（98K~6.7B 参数）的分析显示，参数越多的模型，神经元多义性比例越高，且解释得分（相关系数）随模型规模增长而下降，尤其在深层网络中，多义性导致 “单个神经元语义边界模糊”。

在openai的blog中，研究人员也提出了解决多义性问题的一些方法。研究提出 “寻找可解释方向” 的方法，通过**优化神经元的线性组合**（而非单个神经元）来降低多义性影响。具体做法为初始化随机单位向量 θ，通过坐标上升迭代优化 —— 先寻找能解释该向量激活的自然语言描述，再基于解释得分调整 θ，最终得到 “低多义性的虚拟神经元”。研究提出未来可探索 “非负矩阵分解（NMF）、奇异值分解（SVD）” 等技术，将多义性神经元的激活分解为多个独立的 “单义子成分”，再针对每个子成分生成解释，本质是将 “多义性问题拆解为单义性问题”。


### 特征分解（Feature Decomposition）

### Towards Monosemanticity: Decomposing Language Models With Dictionary Learning

神经网络中最自然的计算单元——神经元本身——却并不是一个适合人类理解的自然单元。这是因为许多神经元具有多义性（polysemanticity）：它们会对看似无关的多种输入产生反应。这种多义性使得作者难以仅通过单个神经元的活动来推理整个网络的行为。在之前的文章Toy Models of Superposition 一文中，作者提出了三种策略，用以在特征被叠加掩盖时，寻找一组稀疏且可解释的特征表示，(1) 构建无叠加的模型，例如通过鼓励激活稀疏性来实现，(2) 使用**字典学习（dictionary learning）**来在存在叠加的模型中寻找一个过完备的特征基，以及 (3) 结合前两者的混合方法。自那篇论文发表以来，作者探索了这三种方法。最终，作者提出了一些反例，这些反例使作者相信：仅依赖稀疏架构（方法1）不足以防止多义性，而标准的字典学习方法（方法2）则存在严重的过拟合问题。

在本文中，作者使用一种称为稀疏自编码器（sparse autoencoder）的弱字典学习算法，从已训练的模型中提取学习到的特征，这些特征相较于模型的神经元本身，构成了更具单义性（monosemantic）的分析单元。本文的目标是详细展示稀疏自编码器如何在两个关键目标上取得令人信服的成果：(1) 从叠加（superposition）中提取可解释的特征，(2) 支持对神经网络内部电路进行基础的可解释性分析。

具体而言，作者取一个单层 Transformer 模型，其 MLP 层包含 512 个神经元，并在 80 亿个数据点上训练稀疏自编码器，以将 MLP 激活分解为相对可解释的特征。扩展因子（expansion factor）从 1×（512 个特征）到 256×（131,072 个特征）不等。作者将主要分析集中在一次特定实验中学习到的 4,096 个特征上，该实验被称为 A/1。

实验结果总结如下。

稀疏自编码器能够提取相对单义的特征。作者从四个角度提供了支持证据，(1) 对少量在特定上下文中激活的特征进行详细分析，并构建相应的计算代理（computational proxies）
(2) 对大量随机抽样的特征进行人工分析，(3) 对自编码器学习到的所有特征的激活进行自动可解释性分析，(4) 对所有特征的 logit 权重 进行自动可解释性分析。此外，后三种分析结果都显示，大多数学习到的特征是可解释的。作者并不声称自己的解释涵盖了特征行为的全部方面，但通过为特征与神经元分别构建一致的可解释性指标（metrics of interpretability），作者在定量上展示了两者的相对可解释性。

稀疏自编码器能生成在神经元基底中“不可见”的可解释特征。作者发现了一些特征（例如对希伯来文字母表征的特征），这些特征在任何神经元的主要激活样本中都未出现，却能被稀疏自编码器有效识别出来。稀疏自编码器的特征可用于干预并引导Transformer的生成行为。例如，当作者激活研究中的 base64 特征 时，模型会生成 Base64 编码文本；激活 阿拉伯文字特征 时，模型则会生成阿拉伯语文本。稀疏自编码器学习到的特征具有一定的普适性（universality）。当将稀疏自编码器分别应用于不同的 Transformer 语言模型时，所得特征之间大多相似——并且彼此之间的相似度要高于它们与各自模型原始神经元的相似度。

随着自编码器规模的增加，特征会发生“分裂（feature splitting）”。当作者逐步将自编码器的宽度从 512（即神经元数量）增加到超过 131,000（即 256× 扩展），发现某些特征会自然地分化成若干“家族”。例如，在较小字典中出现的一个 Base64 特征，在更大的字典中会分裂成三个，具有更细致但仍可解释的功能。不同规模的自编码器因此提供了理解同一对象的不同“分辨率”。仅 512 个神经元即可表示数万个特征。尽管 MLP 层规模很小，作者在扩大稀疏自编码器时仍不断发现新的特征。特征之间可形成类似“有限状态自动机（finite-state automata）”的系统，从而实现复杂行为。例如，作者发现某些特征能够协同工作以生成有效的 HTML 结构。

实验设置如下。

作者选取了单层 Transformer + MLP（ReLU）作为研究目标，称之为“作者尚未理解的最简单语言模型”。他们希望通过分析这层 MLP 的激活，验证是否能用更基础的可解释单元（features）替代“神经元”这一过于粗糙的分析单元。作者提出使用稀疏自编码器（sparse autoencoder）来分解 MLP 激活。并且强调一个关键设定：分解出的特征数远多于神经元数（overcomplete decomposition），因为他们相信 MLP 层通过叠加（superposition）机制压缩了更多语义特征。

我们来采取这样的一种观点，模型的激活可以写成多个“特征方向”的线性组合：
$$ x_j \approx b + \sum_{i} f_i(x_j) d_i $$
激活向量可以由一系列特征向量进行表示。我们使用一个稀疏自编码器来实现这种分解，编码器（encoder）计算特征激活 \\( f_i(x) \\)，解码器（decoder）的列向量代表每个特征的方向\\( d_{i} \\)。如果我们能用稀疏特征把这些激活重新分解出来，就能揭示这些被“叠加”的语义单位，从而理解模型是如何“在少量神经元中存放更多概念”的。



#### 使用SAE,POLYSEMANTIC INTERFERENCE  TRANSFERS AND PREDICTS CROSS-MODEL INFLUENCE

通过利用稀疏自编码器（Sparse Autoencoders, SAEs），作者绘制了两个小模型（Pythia-70M 和 GPT-2-Small）的多义性拓扑结构，以识别那些语义上不相关但在模型内部会相互干扰的 SAE 特征对。作者在四个层面进行了干预（提示词、单词、特征、神经元），并测量了由此在下一个词预测分布中引发的变化，从而揭示了暴露这些模型系统性脆弱性的多义性结构。

### 线性投影（Linear Projections）

### 电路级分析（Circuit Analysis）

### Article Attribution and License
Author: Michael Liu  
Original Link: [https://bv003.github.io/posts/blog/superposition](https://bv003.github.io/posts/blog/superposition)  
License: This article is licensed under CC BY-SA 4.0. Redistribution is not permitted without complying with the license requirements.  

### References
1. Language models can explain neurons in language models. 2023. [link](https://openaipublic.blob.core.windows.net/neuron-explainer/paper/index.html)
2. Circuit Tracing: Revealing Computational Graphs in Language Models. 2025. [link](https://transformer-circuits.pub/2025/attribution-graphs/methods.html)
3. Towards Monosemanticity: Decomposing Language Models With Dictionary Learning.[link](https://transformer-circuits.pub/2023/monosemantic-features/index.html)
4. Signal in the noise: Polysemantic interference transfers and predicts cross-model influence. [link](https://arxiv.org/html/2505.11611v2)