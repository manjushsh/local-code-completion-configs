# Configuring Ollama and Continue VS Code Extension for Local Coding Assistant

## 🔗 Links
[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/manjushsh/local-code-completion-configs)&nbsp;[![GitHub Pages](https://img.shields.io/badge/github%20pages-121013?style=for-the-badge&logo=github&logoColor=white)](https://manjushsh.github.io/local-code-completion-configs/)

## Prerequisites
- [Ollama](https://ollama.com/) installed on your system.
You can visit [Ollama](https://ollama.com/) and [download application](https://ollama.com/download) as per your system.
- AI model that we will be using here is Codellama. **You can use your prefered model**. Code Llama is a model for generating and discussing code, built on top of Llama 2. Code Llama supports many of the most popular programming languages including Python, C++, Java, PHP, Typescript (Javascript), C#, Bash and more. If not installed, you can install wiith following command:  

``` bash 
ollama pull codellama 
```
You can also install `Starcoder 2 3B` for code autocomplete by running:
```bash 
ollama pull starcoder2:3b
```

#### NOTE: It’s crucial to choose models that are compatible with your system to ensure smooth operation and avoid any hiccups.

## Installing Continue and configuring
You can install Continue from [here in VS Code store](https://marketplace.visualstudio.com/items?itemName=Continue.continue).

#### After installation, you should see it in sidebar as shown below:

![Continue in VSCode](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/1.png)

## Configuring Continue to use local model

#### Click on settings icon. It will open a config.json in your editor 

![Configure settings icon](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/2.png)


#### Add configs: 
``` json
{
  "apiBase": "http://localhost:11434/",
  "model": "codellama",
  "provider": "ollama",
  "title": "CodeLlama"
}
```
and also add `tabAutocompleteModel` to config
```json
"tabAutocompleteModel": {
    "apiBase": "http://localhost:11434/",
    "title": "Starcoder2 3b",
    "provider": "ollama",
    "model": "starcoder2:3b"
  }
```

![Update config](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/3.png)

#### Select CodeLlama, which would be visible in dropdown once you add it in config

![Pick modal added in dropdown](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/4.png)

#### Once model is configured, you should be able to ask queastions to the model in chat window

![Chat](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/5.png)

#### And you can also select a codeblock file and ask AI similar to copilot: 

![Code](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/6.png)

## References:
- [Article by Ollama](https://ollama.com/blog/continue-code-assistant)
- [Continue repo on GitHub](https://github.com/continuedev/continue)
- [Continue Docs](https://continue.dev/docs/quickstart)
- [local-code-completion-configs on GitHub](https://github.com/manjushsh/local-code-completion-configs)
- [Ollama models](https://ollama.com/library)
