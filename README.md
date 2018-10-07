# Connect Assistant - Chatfuel

Conecte o Workspace da sua instância do Watson Assistant no Messenger Platform (Facebook) utilizando [Node-RED](https://nodered.org/), uma ferramenta open source. O [Node-RED](https://nodered.org/) será usado para criar uma API que irá conectar o [Chatfuel](https://chatfuel.com/) com o Messenger Platform.

## Pré-requisito

- Ter uma conta (gratuita ou paga) no [IBM Cloud](https://bluemix.net/)
- Ter uma conta (gratuita ou paga) no [Chatfuel](https://chatfuel.com/)
- Ter uma conta no [Facebook](https://facebook.com/) e possuir uma página

## Como conectar seu Watson Assistant no Messenger

### IBM Cloud

1. Acesse a sua conta no [IBM Cloud](https://console.bluemix.net/)

2. Clique em "Catálogo" ou "Criar recursos"
![Acesso ao catálogo](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-01.png)

3. Desça a página até a sessão "Kit de iniciantes" ou filtre no menu lateral esquerdo. Clique no item "Node-RED Starter"
![Node-RED Starter](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-02.png)

4. Digite o nome do seu app. Lembre-se de que o nome do app pode ser usado para definir a URL (**seu-app**.mybluemix.net), mostrado no campo abaixo. Após a configuração do nome e URL, clique no botão "Criar"
![Definir configurações do app](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-03.png)

5. Ao criar o app, espere até finalizar as configurações da sua instância de Node-RED (isso pode levar alguns minutos). Clique no botão "Visite a URL do aplicativo"
![Instância do seu Node-RED](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-04.png)

6. Na sua instância de Node-RED, clique em "Next". Na próxima página, você irá configurar um **usuário** (**username**) e um **senha**  (**password**). Importante lembrar que estes dados serão usados para acessar e editar os seus nós no Node-RED. Após definir o usuário e senha, clique em "Next"
![Configuração do Node-RED](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-05.png)
![Adicionando usuário e senha no Node-RED](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-06.png)

7. Clique em "Next" e depois em "Finish" para finalizar as configurações do seu Node-RED
![Bibliotecas de Node-RED](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-07.png)
![Finalizar configuração no Node-RED](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-08.png)

8. Após configurar o Node-RED, basta clicar no botão "Go to your Node-RED flow editor" para acessar ao editor de nós
![Acessar editor](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-09.png)

9. No editor do Node-RED, clique para abrir o menu no canto superior direito
![Abrir menu](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-10.png)

10. Clique no item "Import" e depois clique no subitem "Clipboard"
![Importar via Clipboard](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-11.png)

11. Acesse o arquivo **nodered.json** neste repositório e copie todo o conteúdo do arquivo. Cole dentro do Clipboard no Node-RED e clique no botão "Import"
![Acesse o arquivo JSON e importe o fluxo no seu Node-RED](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-12.png)

12. Clique duas vezes sobre o nó "Workspace". Este é o nó de Watson Assistant pré-configurado
![Clique duas vezes no nó de Watson Assistant](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-13.png)


13. Insira as credenciais do seu Watson Assistant, como **username**, **password** e **workspace_id** nos campos abaixo. Clique o botão "Done" na parte superior
![Configurando o nó de Watson Assistant](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-14.png)

14. Por final, clique no botão "Deploy" no canto superior direito da tela.
![Subir em produção](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-15.png)

### Chatfuel

1. Acesse a sua conta no [Chatfuel](https://chatfuel.com/)

2. Clique no botão "Create from Template" para criar um novo chatbot
![Criar um novo chatbot](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-16.png)

3. Clique em "Blank Bot"
![Criar um novo chatbot do zero](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-17.png)

4. Clique no novo item (geralmente ele começa com o nome "Blank Bot" mas pode ser alterado nas configurações)
![Acessar o chatbot](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-18.png)

5. Dentro do **Welcome Message**, remova o card existente. Neste caso, usaremos o nó de Welcome do Watson Assistant
![Remover card de Welcome Message](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-19.png)

6. Clique em "Default Answer" e remova o card existente. Iremos conectar a nossa API (Application Programming Interface) importada no Node-RED, onde contem o Watson Assistant, no [Chatfuel](https://chatfuel.com/).
![Remover card de Default Answer](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-20.png)

7. Na seção "ADD A CARD", clique no ícone de mais (+) para abrir o menu com todas as opções
![Abrir menu com opções de cards](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-21.png)

8. Selecione o item "User Input". Ele será usado para armazenar a mensagem do usuário em uma variável no [Chatfuel](https://chatfuel.com/)
![Adicionar card de User Input](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-22.png)

9. No campo "SAVE ANSWER TO ATTRIBUTE", coloque no meio das chaves a palavra **mensagem**. Após configurar a variável, clique novamente no ícone de mais (+)
![Salvar mensagens na variável mensagem](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-23.png)

10. Selecione o item "JSON API". Este é o item que irá enviar todas as mensagens para o Node-RED que irá enviar para o Watson Assistant para analisar o texto em linguagem natural
![Adicionar o card de JSON API](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-24.png)

11. No campo "URL" adicione a URL da API seu Node-RED junto com dois dados: **mensagem** e **usuario**. Ele ficará dessa forma, por exemplo:

```
https://connect-assistant-chatfuel.mybluemix.net/bot?mensagem={{mensagem}}&usuario={{messenger user id}}
```

12. Após configurar a seção de JSON API com a API do seu Node-RED, clique no botão "CONNECT TO FACEBOOK" e selecione uma página que você gerencia para integrar no seu chatbot. Clique em "TEST THIS CHATBOT" e aproveite o seu chatbot no Facebook Messenger Platform!
![Conectar seu chatbot em uma página e teste](https://github.com/victorshinya/connect-assistant-chatfuel/blob/master/img/connect-assistant-chatfuel-25.png)
