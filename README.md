[![](https://img.shields.io/badge/IBM%20Cloud-powered-blue.svg)](https://bluemix.net)
[![Platform](https://img.shields.io/badge/platform-nodejs-lightgrey.svg?style=flat)](https://developer.ibm.com/node/)

# Conecte o seu Watson Assistant no Facebook Messenger | Connect Assistant Chatfuel

Connecte o seu chatbot com [Watson Assistant](https://www.ibm.com/cloud/watson-assistant/) no [Facebook Messenger](https://developers.facebook.com/) com a plataforma do [Chatfuel](https://chatfuel.com/) e a ferramenta open source do [Node-RED](https://nodered.org/). Caso não tenha um chatbot ou não saiba como construir um, acesse e leia o [blog sobre criação de chatbot usando Watson Assistant](https://medium.com/ibmdeveloperbr/watson-assistant-como-criar-o-seu-chatbot-usando-skills-e-assistants-755b4677984b/) e também o passo a passo de [como subir em uma página no Messenger](https://medium.com/ibmdeveloperbr/integre-seu-watson-assistant-no-facebook-via-chatfuel-925b9b20e4be).

![](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/doc/source/images/architecture.jpg)

## Componentes e tecnologias usadas

* [Node-RED](https://nodered.org/): ferramenta de criação de serviços baseado em fluxo.
* [Chatfuel](https://chatfuel.com/): plataforma de construção de chatbot com inteligência artificial. Foi usada como hub para publicação do bot no Facebook Messenger.

## Como subir na nuvem - IBM Cloud

Para subir na IBM Cloud, basta ter uma conta na IBM Cloud e criar uma instância do Node-RED. A partir da sua instância, você irá importar o fluxo e configurar o [Chatfuel](https://chatfuel.com/). Caso ainda não conheça, acesse o blog no Medium da [IBM Developer Brasil](https://medium.com/ibmdeveloperbr/o-que-e-a-ibm-cloud-e-como-subir-a-sua-primeira-aplicacao-na-nuvem-41bfd260a2b7) para entender mais.

## Como instalar e configurar localmente

Para instalar e executar a aplicação, é necessário ter o [Node-RED](https://nodered.org/) instalado no seu computador e seguir o passo a passo abaixo.

### 1. Baixe o repositório

```sh
git clone https://github.com/victorshinya/connect-assistant-chatfuel.git
cd connect-assistant-chatfuel
```

### 2. Importe o fluxo do Node-RED no arquivo **nodered.json**

### 3. Faça o deploy

### 4. Configure no Chatfuel e teste o seu bot no Facebook Messenger

## License

MIT License

Copyright (c) 2018 Victor Kazuyuki Shinya
