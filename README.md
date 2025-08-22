# Ollama Python Package - Local Experiments
My experiments using the Ollama python package to run models locally on an M4 Macbook Air, 16GB RAM - in a Jupyter notebook.
<br>
<br>
- Qwen3: 4B, 8B, 14B<br>
- Gemma3: 12B
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

Qwen3 30B Ollama:
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
