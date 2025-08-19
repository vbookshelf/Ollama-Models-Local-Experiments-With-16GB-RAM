## Exp3 - Use Qwen3 models in a simple ReAct workflow

### Objective
- Use the Qwen 3 models as part of a ReAct workflow
- ReAct is an alternative approach to function calling
- Check that these models are able to reliably follow the ReAct instructions in the system message.
- This is a simple "dog weights" example

### Notes
- All Qwen models performed very well.
- Even the small 4B model performed brilliantly.
- I did not tell the model how to handle the condition where a function does not need to be called however, the model chose the correct way forward by itself. The 4B model is also able to do this. In previous testing the non-thinking Llama 70b model failed when it encountered this condition. My guess is that although thinking slows increases the inference time, it also adds strong capability to small models.
- The code includes a chat loop.
