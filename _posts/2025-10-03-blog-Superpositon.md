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

在openai的blog中，研究人员也提出了解决多义性问题的一些方法。研究提出 “寻找可解释方向” 的方法，通过**优化神经元的线性组合**（而非单个神经元）来降低多义性影响。具体做法为初始化随机单位向量 θ，通过坐标上升迭代优化 —— 先寻找能解释该向量激活的自然语言描述，再基于解释得分调整 θ，最终得到 “低多义性的虚拟神经元”。


### Article Attribution and License
Author: Michael Liu  
Original Link: [https://bv003.github.io/posts/blog/superposition](https://bv003.github.io/posts/blog/superposition)  
License: This article is licensed under CC BY-SA 4.0. Redistribution is not permitted without complying with the license requirements.  

### References
1. Bills, S., Cammarata, N., Mossing, D., Tillman, H., Gao, L., Goh, G., Sutskever, I., Leike, J., Wu, J., Saunders, W. Language models can explain neurons in language models. 2023. [https://openaipublic.blob.core.windows.net/neuron-explainer/paper/index.html](https://openaipublic.blob.core.windows.net/neuron-explainer/paper/index.html)
2. Ameisen, E., Lindsey, J., Pearce, A., Gurnee, W., Turner, N. L., Chen, B., Citro, C., Abrahams, D., Carter, S., Hosmer, B., Marcus, J., Sklar, M., Templeton, A., Bricken, T., McDougall, C., Cunningham, W., Henighan, T., Jermyn, A., Jones, A., Persic, A., Qi, Z., Thompson, T. B., Zimmerman, S., Rivoire, K., Conerly, T., Olah, C., Batson, J. Circuit Tracing: Revealing Computational Graphs in Language Models. 2025. [https://transformer-circuits.pub/2025/attribution-graphs/methods.html](https://transformer-circuits.pub/2025/attribution-graphs/methods.html)