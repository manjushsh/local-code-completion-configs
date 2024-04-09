## 🔗 Links
[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/manjushsh/local-code-completion-configs) [![GitHub Pages](https://img.shields.io/badge/github%20pages-121013?style=for-the-badge&logo=github&logoColor=white)](https://manjushsh.github.io/local-code-completion-configs/)

## Prerequisites
- [Ollama](https://ollama.com/) installed on your system.
You can visit [Ollama](https://ollama.com/) and download application as per your system.
- AI model that we will be using here is Codellama. Code Llama is a model for generating and discussing code, built on top of Llama 2. It’s designed to make workflows faster and efficient for developers and make it easier for people to learn how to code. It can generate both code and natural language about code. Code Llama supports many of the most popular programming languages used today, including Python, C++, Java, PHP, Typescript (Javascript), C#, Bash and more. If not installed, you can install wiith following command: 

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

#### Click on settings icon: 

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

![Update config](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/3.png)

#### You should be able to select model you added in config now. So select CodeLlama. 

![Pick modal added in dropdown](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/4.png)

#### And you can also chat as normal as shown below

![Chat](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/5.png)

#### And you can also select a codeblock file and ask AI: 

![Code](https://raw.githubusercontent.com/manjushsh/local-code-completion-configs/main/public/assets/6.png)

## References:
- [Continue repo on GitHub](https://raw.githubusercontent.com/continuedev/continue)
- [Continue Docs](https://continue.dev/docs/quickstart)
- [local-code-completion-configs on GitHub](https://github.com/manjushsh/local-code-completion-configs)
- [Ollama models](https://ollama.com/library)
