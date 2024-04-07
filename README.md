
# Setting up Ollama and Continue to get local coding assistant

## Prerequisites
- [Ollama](https://ollama.com/) installed on your system.
You can visit [Ollama](https://ollama.com/) and download application as per your system.
- AI model in this case we are using Codellama. 
You can install it with 
``` bash 
ollama pull codellama 
```
You can optionally install starcoder-3b for code autocomplete by running 
```bash 
ollama pull starcoder-3b
```

## Installing Continue and configuring
You can install Continue from [here in VS Code store](https://marketplace.visualstudio.com/items?itemName=Continue.continue).

After installation, you should see it in sidebar as shown below:
![Continue in VSCode](https://github.com/manjushsh/local-code-completion-configs/blob/main/assets/1.png)

## Configuring Continue to use local model

- Click on settings icon: ![Configure settings icon](https://github.com/manjushsh/local-code-completion-configs/blob/main/assets/2.png)
- Add configs: 
``` json
{
      "apiBase": "http://localhost:11434/",
      "model": "codellama",
      "provider": "ollama",
      "title": "CodeLlama"
    },
```
![Update config](https://github.com/manjushsh/local-code-completion-configs/blob/main/assets/3.png)
- You should be able to select model you added in config now. So select CodeLlama. ![Pick modal added in dropdown](https://github.com/manjushsh/local-code-completion-configs/blob/main/assets/4.png)
And you can also chat as normal ![Chat](https://github.com/manjushsh/local-code-completion-configs/blob/main/assets/5.png)
or file level code ![Code](https://github.com/manjushsh/local-code-completion-configs/blob/main/assets/6.png)
