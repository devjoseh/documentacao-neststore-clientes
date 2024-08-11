# Bem-Vindo(a)
## 👑 _Documentação - Suggestion Bot - V14.x_

# 🤖 Instalando e Iniciando o BOT

Caso deseje iniciar o bot em sua máquina local, inicie o arquivo `install.bat` que está na raiz do projeto para instalar todos os módulos necessários. `Certifique-se de ter o NodeJS instalado no seu pc`

Utilize o arquivo `start.bat` para iniciar o bot sem a necessidade do VSCode aberto. Certifique-se de iniciá-lo somente após a instalação de todos os módulos e a configuração de todos os arquivos.

## 💻 Pré-requisitos

Antes de instalar, verifique se sua máquina atende aos seguintes requisitos:

* [Nodejs](https://nodejs.org/en/) v16.9.0 ou superior

# 🔧 Configurando o BOT

Vá para a raiz do projeto e renomeie o arquivo `.env.example` para `.env` e coloque todas as informações necessárias

```bash
TOKEN=
# Bot token

ACCESS_TOKEN=
# Token de acesso do Mercado Pago

GUILD_ID=
# ID do servidor principal

CLIENT_ID=
# Id do bot

OWNER_ID=
# Id do dono do bot
```

Para alterar algumas informações de como as embeds do bot são criadas, vá para `configs > settings`

```js
const settings = {
    color: "#2B2D31",
    // Cor de todas as embeds do bot em formato hex
    titulo: "Nest Store 👑",
    // Titulo que aparecerá em todas as embeds
    footer: "Copyright © 2022-2024, Nest Store. Todos os direitos reservados.",
    // Footer que aparecerá em todas as embeds

    cooldowns: {
        message: "Aguarde: `<duration>` para executar o comando novamente!"
    },
    // Mensagem de erro que é mostrada quando um comando está em delay

    erromsg: {
        titulo: "🤔 Encontrei um problema!"
    },
    // Mensagem de erro que é mostrada quando algum erro acontece em um comando

    suggestionEmbedImage: ""
    // Imagem que aparece na embed que os usuários clicam para enviar uma sugestão.
    // Deixe vazio "" para não aplicar nenhuma imagem;
};
```
## Arquivos de Configuração

### Arquivo `configs > icons.js`

Todas as configurações dos emojis usados pelo bot. Arquivo já configurado, mas pode ser alterado como desejar.

## Status do Bot

Para alterar alguma informação do status do bot, vá para a pasta `events > client > ready` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.<br>
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).<br>
`timer:` Tempo em segundos para a troca de mensagens e status.<br>

`online` = status online<br>
`dnd` = status não perturbe<br>
`idle` = status ausente<br>

em `let timer` é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos

## Configurando o banco de dados

Vá para a pasta `events > database > connect.js`
Nesse arquivo é onde deve-se configurar o banco de dados. Segue o tutorial:

1. [Clique aqui](https://firebase.google.com/docs?hl=pt&authuser=0) para acessar o firebase
2. No canto superior direito, clique em `ir para o console`
3. Clique no botão de `adicionar projeto`
4. Coloque o nome da sua loja ou qualquer outro
5. Desative a opção `Ativar o Google Analytics neste projeto`
6. Clique em `criar projeto`
7. No menu lateral esquerdo, clique em `criação`
8. Selecione a opção `Realtime Database`
9. Clique em `criar banco de dados`
10. Verifique se está selecionado `Estados Unidos` e clique em `proxima`
11. Selecione `iniciar no modo bloqueado` e clique em `ativar`
12. Em baixo de `Realtime Database`, clique em `Regras`
13. Altere: `".read"` de `false` para `true`. Faça o mesmo com `".write"`
14. Clique em publicar
15. Após isso, clique em `Visão geral do projeto` no lado superior esquerdo
16. Clique no botão que se parece com: `</>`
17. Em apelido do app, coloque qualquer nome e não marque a caixa `Configure também...`
18. Clique em registrar app
19. Na opção `Usar o npm`
20. Copie esse código:

```
const firebaseConfig = {
  apiKey: "",
  authDomain: "",
  databaseURL: "",
  projectId: "",
  storageBucket: "",
  messagingSenderId: "",
  appId: ""
};
```

21. No bot, vá para: `events > database > connect` e substitua o código `firebaseConfig` por esse que você copiou
22. Pronto, banco de dados configurado :D

## 📂 Comandos

Nome | Categoria | Descrição
| - | - | - |
[/canal](README.md) | Configurações | Seta um canal em alguma configuração.
[/cargo](README.md) | Configurações | Seta um cargo em alguma configuração.
[/configs](README.md) | Configurações | Mostra todas as configurações atuais.
[/desativar](README.md) | Configurações | Desativar alguma das configurações.
[/ping](README.md) | Geral | Mostra o tempo de resposta do bot.
[/help](README.md) | Staff | Visualiza todos os comandos do bot.
[/painel](README.md) | Staff | Envia a embed de alguma opção do painel.
[/sugestao](README.md) | Staff | Aprova ou Nega uma sugestão feita no servidor.