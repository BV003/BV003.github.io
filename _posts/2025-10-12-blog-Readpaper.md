---
title: 'Notes on Two Papers about Chain-of-Thought and LLM Reliability'
date: 2025-10-12
permalink: /posts/blog/readpaper/1
---

Two recent papers challenge how we evaluate LLMs — one questions chain-of-thought in planning, the other doubts model self-reports. I summarize their insights and try to extract their experiments for future agent training.

<!-- excerpt -->

### An Analysis of CoT in Planning

#### research question
Does chain-of-thought (CoT) prompting truly enable large language models (LLMs) to learn generalizable algorithmic reasoning abilities, or does it merely rely on highly specific, pattern-matching prompts?

#### experiment setup

The study focuses on the Blocksworld domain, where a set of blocks must be rearranged from an initial configuration to a specified goal configuration through a sequence of actions. In some experiments, the task is further simplified by considering only instances where all blocks start on the table and the goal is a single stack. These tasks require minimal reasoning—only identifying the bottom block and then stacking the remaining blocks in the order specified by the goal. 

Different levels of Chain-of-Thought (CoT) prompts were designed, each more specific and containing more task-relevant knowledge than the previous: a zero-shot version, a general progression proof, a domain-specific suboptimal Blocksworld algorithm, a “table-to-stack” simplification of that algorithm, and a lexicographically defined simplified variant.

Experiments were conducted on three models: GPT-4, Claude-3-Opus, and GPT-4-Turbo. The models output sequences of actions in natural language, which are converted into PDDL format and automatically verified using the VAL (PDDL Validator) tool to determine whether the initial state can reach the goal state. Performance was evaluated across multiple dimensions, including accuracy, generalization, robustness, and self-consistency.

#### conclusion
The performance improvements from Chain-of-Thought (CoT) prompts do not arise from the models genuinely learning algorithmic reasoning; rather, they rely on carefully crafted, task-specific prompt templates. Large language models (LLMs) are generally incapable of solving even simple planning problems, and the results indicate that CoT approaches only enhance performance when the hand-annotated examples closely match the target queries. As the size of the goal stack increases, accuracy drops sharply—regardless of the specificity of the prompt.

### Questioning the Survey Responses of Large Language Models

#### research question
Current research often compares LLMs’ survey responses with human data to infer model characteristics or values, but this approach lacks systematic validation. This study examines whether LLM responses reflect model properties, how closely they match human survey data, the validity of alignment metrics, and whether instruction tuning or RLHF improves consistency, as well as the generalizability of findings to other surveys like ATP, GAS, and WVS.


#### experiment setup

Reference surveys and data: The study uses the 2019 U.S. Census Bureau’s American Community Survey (ACS) as the core benchmark, selecting 25 multiple-choice questions covering demographics (gender, age, race), education, health insurance, marital status, employment, and income. The 2019 ACS microdata (~3.2 million anonymized responses) serve as the human reference. Additional datasets, including the American Trends Panel (ATP), Global Attitudes Survey (GAS), World Values Survey (WVS), and 2016 American National Election Study (ANES), are used to test generalizability.

Model selection: 43 LLMs of varying types and sizes (110M–175B parameters) were tested, including base models (GPT-2, GPT-Neo, Pythia, MPT, Llama 2/3, GPT-3) and instruction-tuned models (MPT-7B Instruct, GPT-NeoX 20B Instruct, Llama 2/3 Chat, GPT-4).

Prompting and response collection: Standardized multiple-choice prompts of the form
“Question: <content> \n A. <option 1> \n B. <option 2> … \n Answer:”
were used. The next-token probabilities for each option were normalized to obtain the model’s “survey response.”

Randomized option order: To mitigate label and position biases (e.g., “A-bias”), option orders were randomly shuffled for each question.

Metrics: Normalized entropy measures the dispersion of model responses (1 = fully uniform; lower values indicate concentration). KL divergence quantifies similarity between model and human distributions (or uniform), with lower values indicating closer alignment. Average KL was computed against U.S. national, state-level, and uniform distributions to assess consistency with human data.


#### conclusion
Research indicates that using LLMs to answer human surveys has fundamental limitations. Responses are dominated by systematic biases, weakly tied to question semantics, and remain far from human data even after instruction tuning or RLHF. Alignment metrics largely reflect human subgroup response entropy rather than model properties. Thus, applying human survey tools to LLMs is unreliable, and future studies should design methods tailored to LLMs to assess bias and representativeness.




### Article Attribution and License
Author: Michael Liu  
Original Link: [https://bv003.github.io/posts/blog/readpaper/1](https://bv003.github.io/posts/blog/readpaper/1)  
License: This article is licensed under CC BY-SA 4.0. Redistribution is not permitted without complying with the license requirements.  