---
title: "MELL: Memory Efficient Large Language Model Serving System via Online Dynamic Scheduling"
collection: publications
category: conferences
permalink: /publication/2024-12-06-MELL-Memory-Efficient-Large-Language-Model-Serving-System-via-Online-Dynamic-Scheduling
# excerpt: 'This paper is about fixing template issue #693.'
date: 2024-12-06
venue: 'INFOCOM 2025'
# paperurl: '/files/mell-infocom-2025.pdf'
# citation: 'Your Name, You. (2024). &quot;Paper Title Number 3.&quot; <i>GitHub Journal of Bugs</i>. 1(3).'
---

Serving large language models (LLMs) for massive users is challenged by the significant memory footprint of the transient state, known as the \emph{key-value (KV) cache}, which scales with sequence length and number of requests. 
Instead of renting or buying more expensive GPUs, the load imbalance of the KV cache across GPUs, coupled with recent advances in inter-GPU communication, provides an opportunity to serve more requests via request migration. 
However, high migration overhead and unpredictable request patterns make it challenging. 
Therefore, this paper proposes \textsc{Mell}, a memory-efficient LLM serving system via \emph{multi-GPU KV cache management}. 
It saves the number of GPUs needed in the system by considering the dynamic KV cache load and the costly request migration. 
Specifically, we first develop an adaptive request migration mechanism to balance the computational and communication overheads and adapt to diverse resource conditions. 
Then, we design an online algorithm tailored to a multi-LLM request and multi-GPU scheduling problem with migration enabled.
It aims to minimise the required GPUs while limiting the number of migrations.
% and achieves a competition ratio of $4/3$. 
Finally, we implement a prototype of \textsc{Mell} and demonstrate that it reduces the number of GPUs by $31\%$ and increases the GPU utilization by $43\%$ at most compared to existing LLM serving systems.
