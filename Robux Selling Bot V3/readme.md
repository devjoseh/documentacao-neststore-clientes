# Bem-Vindo(a)
## 👑 _Documentação - Trivia Bot - V14.x_

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

```bash
const settings = {
    color: "#2B2D31",
    # Cor de todas as embeds do bot em formato hex
    titulo: "Nest Store 👑",
    # Titulo que aparecerá em todas as embeds
    footer: "Copyright © 2022-2024, Nest Store. Todos os direitos reservados.",
    # Footer que aparecerá em todas as embeds

    cooldowns: {
        message: "Aguarde: `<duration>` para executar o comando novamente!"
    },
    # Mensagem de erro que é mostrada quando um comando está em delay

    erromsg: {
        titulo: "🤔 Encontrei um problema!"
    }
    # Mensagem de erro que é mostrada quando algum erro acontece em um comando
};
```
## Arquivos de Configuração

### Arquivo `configs > embeds.js`

Todas as configurações das embeds enviadas pelo bot. Arquivo já configurado, mas pode ser alterado como desejar.

### Arquivo `configs > icons.js`

Todas as configurações dos emojis usados pelo bot. Arquivo já configurado, mas pode ser alterado como desejar.

### Arquivo `configs > paymentConfig.js`

`email:` Email do pix cadastrado no mercadopago. <br>
`nome:` Primeiro nome do titular da conta. <br>
`sobrenome:` Sobrenome do titular da conta. <br>

### Arquivo `configs > store.js`

Configurações relacionadas a todo o sistema da loja.

#### Em atendimento:

```
dias: {
    inicio: "Segunda", // Dia de início dos atendimentos
    fim: "Sexta" // Dia que acaba os atendimentos
},
horario: {
    inicio: "10:00", // Horário de inicio dos atendimentos
    fim: "19:00" // Horário que acaba os atendimentos
}
```

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

## Pegando access token (credencial)

1. [Clique aqui](https://mercadopago.com.br) para acessar o mercado pago
2. Faça login na sua conta
3. No menu lateral esquerdo, procure `Seu negócio`, clique e vá em `Configurações`
4. Faça a verificação
5. Na caixa `Gestão e Administração`, clique em `Credenciais`
6. Selecione `Credenciais de Produção`
7. O código de acesso é o código `Access Token`
8. **ATENÇÃO: NÃO COMPARTILHE ESTE TOKEN COM NINGUÉM**

## 📂 Comandos

Nome | Categoria | Descrição
| - | - | - |
[/canal](README.md) | Configurações | Seta um canal em alguma configuração.
[/cargo](README.md) | Configurações | Seta um cargo em alguma configuração.
[/configs](README.md) | Configurações | Mostra todas as configurações atuais.
[/configurar](README.md) | Configurações | Configura algum dos sistemas
[/desativar](README.md) | Configurações | Desativar alguma das configurações.
[/manutencao](README.md) | Configurações | Coloca ou remove a loja em manutenção.
[/preco](README.md) | Configurações | Altera o valor dos Robux ou Gamepass.
[/status](README.md) | Configurações | Altera o status da loja para Online ou Offline.
[/perfil](README.md) | Geral | Mostra as informações do usuário/outra pessoa.
[/ping](README.md) | Geral | Mostra o tempo de resposta do bot.
[/ranking](README.md) | Geral | Mostra o top 10 pessoas com mais dinheiro gasto no servidor.
[/valor](README.md) | Geral | Visualiza o preço de uma quantia de robux.
[/categoria](README.md) | Staff | Listar, editar ou deletar uma categoria de jogo.
[/consultar](README.md) | Staff | Visualiza as informações de um pedido específico.
[/cupom](README.md) | Staff | Listar, editar ou deletar um cupom.
[/demanda](README.md) | Staff | Visualiza quantos robux estão pendentes para entrega.
[/entregar](README.md) | Staff | Faz a entrega de um pedido.
[/estatisticas](README.md) | Staff | Visualiza as estatisticas da loja em geral.
[/help](README.md) | Staff | Visualiza todos os comandos do bot.
[/painel](README.md) | Staff | Envia a embed de alguma opção do painel.
[/pedidos](README.md) | Staff | Lista todos os pedidos concluidos e pendentes.
