# AI LLM `Attention` Model Notes

## Attention in Machine Learning
- Definition: A technique that mimics cognitive attention, enhancing important parts of the input data and diminishing others[^1^].
- Types of Attention[^7^][^8^][^11^]
    - Self-Attention: Relates different positions of a sequence to compute a representation of that sequence[^5^].
    - Multi-Head Attention: Allows models to focus on different parts of the input using assigned weights[^8^].
- Visualization: Attention weights and outputs can be interpreted and visualized to understand the model's focus[^3^].

## vLLM and PagedAttention
- vLLM: An open-source library for fast LLM inference and serving[^2^][^4^].
    - Command: `git clone https://github.com/ucberkeley/vllm.git`
- PagedAttention: A new attention algorithm that effectively manages attention keys and values[^2^][^4^].
    - Benefits: Delivers up to 24x higher throughput than HuggingFace Transformers[^2^][^4^].

## Applications of Attention in AI
- Machine Translation: Attention mechanisms help models focus on the most relevant parts of the input and output sequences[^3^][^9^].
- Text Summarization, Image Captioning, and Speech Recognition: Attention can improve the performance and accuracy of these tasks[^3^].
- Neural Mechanisms: Understanding of top-down divided and selective spatial attention in visual and auditory perception[^6^].

## Transformers
- Transformers: A game-changing architecture in the field of NLP[^10^].
- Self-Attention in Transformers: Describes a transformer model’s ability to attend to various parts of an input sequence when making predictions[^5^][^10^].

## Attention in Deep Learning
- Role of Attention: Guides the algorithm to focus on the important parts of the data[^7^].
- Components of an Attention-Based System[^7^]
    - A process that reads the raw data and converts them into distributed representations.
    - An attention mechanism that computes a weighted sum of these representations.
    - A process that takes the output of the attention mechanism and generates a final output.

[^1^]: [Link](https://en.wikipedia.org/wiki/Attention_(machine_learning))
[^2^]: [Link](https://www.symphora.com/2023/06/vllm-easy-fast-and-cheap-llm-serving-with-pagedattention/)
[^3^]: [Link](https://www.linkedin.com/advice/0/how-do-you-interpret-visualize-attention)
[^4^]: [Link](https://bardai.ai/artificial-intelligence/vllm-pagedattention-for-24x-faster-llm-inference/)
[^5^]: [Link](https://fourweekmba.com/self-attention/)
[^6^]: [Link](https://journals.sagepub.com/doi/10.26599/BSA.2023.9050008)
[^7^]: [Link](https://medium.com/the-research-nest/understanding-attention-in-machine-learning-96c187f76cd8)
[^8^]: [Link](https://www.analyticsvidhya.com/blog/2023/06/understanding-attention-mechanisms-using-multi-head-attention/)
[^9^]: [Link](https://www.geeksforgeeks.org/ml-attention-mechanism/)
[^10^]: [Link](https://ultragorira.github.io/2023/07/03/Transformers_Attention_is_all_you_need.html)
[^11^]: [Link](https://towardsdatascience.com/intuitive-understanding-of-attention-mechanism-in-deep-learning-6c9482aecf4f)
