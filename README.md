## Thinking Isn't an Illusion

This is the official implementation of the paper "**Thinking Isn’t an Illusion: Overcoming the Limitations of Reasoning Models via Tool Augmentations**". You can find our paper on [arXiv](https://arxiv.org/).

Our paper revisits recent claims that Large Reasoning Models (LRMs) fail to outperform standard LLMs on reasoning tasks, as suggested by [Apple's "thinking-illusion" benchmark](https://arxiv.org/pdf/2506.06941). Differing from Apple's study, we introduce **tool augmentation**, including Python interpreter and scratchpads to the LLM/LRM evaluation process. 

## Environment Requirement

All code can be run directly in [Google Colab](https://colab.research.google.com/) with your own LLM API key. 

- For **DeepSeek-V3** and **DeepSeek-R1**, we use the official model API via [DeepSeek API](https://platform.deepseek.com/api_keys).  
- For **Qwen 3** and **Qwen 3 Thinking**, we use the model API via [OpenRouter](https://openrouter.ai/settings/keys).


## Main Results

On River Crossing and Blocks World, we observe a clear advantage of LRMs over LLMs under tool‑augmentation.

### River Crossing (5 runs)

| Tool Usage          | Model         | N=3   | N=5   | N=7   | N=9   | N=11  | N=13  |
|---------------------|---------------|-------|-------|-------|-------|-------|-------|
| **Think‑and‑Execute** [[paper]](https://arxiv.org/pdf/2404.02575) | DeepSeek‑V3  | 0/5   | 0/5   | 0/5   | 0/5   | 0/5   | 0/5   |
|                     | DeepSeek‑R1   | 0/5   | 0/5   | 0/5   | 0/5   | 0/5   | 0/5   |
| **PoT** [[paper]](https://openreview.net/pdf?id=YfZ4ZPt8zd)             | DeepSeek‑V3   | 0/5   | 0/5   | 0/5   | 0/5   | 0/5   | 0/5   |
|                     | DeepSeek‑R1   | **<u>4/5</u>** | **<u>4/5</u>** | **<u>4/5</u>** | **<u>4/5</u>** | **<u>4/5</u>** | **<u>4/5</u>** |
| **Scratchpad**  | DeepSeek‑V3   | 0/5   | 0/5   | 0/5   | 0/5   | 0/5   | 0/5   |
|                     | DeepSeek‑R1   | **<u>1/5</u>**| 0/5   | 0/5   | 0/5   | 0/5   | 0/5   |

### Blocks World (5 runs)

| Tool Usage          | Model         | N=3   | N=5   | N=7        | N=9        | N=11       | N=13       |
|---------------------|---------------|-------|-------|------------|------------|------------|------------|
| **Think‑and‑Execute** [[paper]](https://arxiv.org/pdf/2404.02575)| DeepSeek‑V3  | 5/5   | 5/5   | 0/5        | 0/5        | 0/5        | 0/5        |
|                     | DeepSeek‑R1   | 5/5   | 4/5   | **<u>2/5</u>** | **<u>2/5</u>** | **<u>1/5</u>**| **<u>1/5</u>** |
| **PoT** [[paper]](https://openreview.net/pdf?id=YfZ4ZPt8zd)             | DeepSeek‑V3   | 1/5   | 1/5   | 1/5        | 1/5        | 1/5        | 1/5        |
|                     | DeepSeek‑R1   | **<u>5/5</u>** | **<u>5/5</u>** | **<u>5/5</u>**  | **<u>5/5</u>**  | **<u>5/5</u>**  | **<u>5/5</u>**  |
| **Scratchpad**   | DeepSeek‑V3   | 5/5   | 1/5   | 0/5        | 0/5        | 0/5        | 0/5        |
|                     | DeepSeek‑R1   | <u>5/5</u> | **<u>5/5</u>**| **<u>3/5</u>**  | **<u>4/5</u>**  | **<u>4/5</u>**  | 0/5        |

*For the complete list of results, please refer to our paper.*

## BibTeX

If you find our work useful in your research, please cite the following in your manuscript:


