# Ollama Python Package - Local Experiments
My experiments using the Ollama python package to run models locally on an M4 Macbook Air, 16GB RAM - in a Jupyter notebook.
The goal is to build intuition.
<br>
<br>
- Qwen3: 4B, 8B, 14B<br>
- Gemma3: 12B
- Phi4: 14B
<br>

### Qwen3

Qwen3 4B Ollama:
- parameters: 4.02B
- quantization: Q4_K_M
- size: 2.5GB
- context: 256k
- thinking: Yes

Qwen3 8B Ollama:
- parameters: 8.19B
- quantization: Q4_K_M
- size: 5.2GB
- context: 40k
- thinking: Yes


Qwen3 14B Ollama:
- parameters: 14.8B
- quantization: Q4_K_M
- size: 9.3GB
- context: 40k
- thinking: Yes

Qwen3 30B Ollama: (Runs on 16GB Mac, but very slow.)
- parameters: 30.5B
- quantization: Q4_K_M
- size: 19GB
- context: 256k
- thinking: Yes

### Gemma3

Gemma3 12B Ollama:
- parameters: 12.2B
- quantization: Q4_K_M
- size: 8.16GB
- context: 128k
- thinking: No

### Phi4

Phi4 14B Ollama:
- parameters: 14.7B
- quantization: Q4_K_M
- size: 9.16GB
- context: 16k
- thinking: No
  
<br>

## Experiments

- Exp1 - Set up the UV project folder and Python environment on Mac<br>
(Everything is being run locally on the Mac desktop)<br>
https://github.com/vbookshelf/Qwen3-Ollama-Local-Experiments/tree/main/Exp1%20-%20Set%20up%20the%20UV%20project%20folder%20and%20python%20environment

- Exp2 - Simple Qwen3 Ollama Python code in a Jupyter notebook<br>
(Set up the code for chat inference)<br>
https://github.com/vbookshelf/Qwen3-Ollama-Local-Experiments/tree/main/Exp2%20-%20Simple%20ollama%20python%20code%20in%20a%20jupyter%20notebook

- Exp3 - Use Qwen3 models in a simple ReAct workflow<br>
(Using the simple "dog weights" example. Includes a python chat loop.)<br>
https://github.com/vbookshelf/Qwen3-Ollama-Local-Experiments/tree/main/Exp3%20-%20Use%20Qwen3%20in%20a%20simple%20ReAct%20lworkflow

- Exp4 - Qwen3 research assistant w RAG search and Tavily web search<br>
(ReAct workflow)<br>
https://github.com/vbookshelf/Ollama-Models-Local-Experiments-With-16GB-RAM/tree/main/Exp4%20-%20Qwen3%20research%20assistant%20w%20RAG%20search%20and%20web%20search

- Exp5 - Qwen3 Email responder llm workflow<br>
https://github.com/vbookshelf/Ollama-Models-Local-Experiments-With-16GB-RAM/tree/main/Exp5%20-%20Qwen3%20Email%20responder%20llm%20workflow

- Exp6 - Two agents chatting in a panel discussion with the user as moderator<br>
https://github.com/vbookshelf/Ollama-Models-Local-Experiments-With-16GB-RAM/edit/main/README.md



## Notes

- A models ability to follow the ouput formatting instructions given in the system message, can degrade as the context memory fills up. Especially relevant when RAG search or web search results are added to the context memory.
- Almost all the errors that occur are related to incorrect JSON output formatting i.e. the model's output is not being formatted in the specified way or the model is not outputting JSON at all. As a result, when using a ReAct workflow, the router cannot route to the next step and the code fails. One solution could be to let the model output text and also make the router an LLM so that it can simple read the plain text output and decide what to do.
