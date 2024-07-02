# Bem-Vindo(a)
## 👑 _Documentação - Find Suspect User - V13.x & V14.x_

> [!NOTE]
> Esse bot foi desenvolvido para estudos e não tem intensão de invadir ou de alguma forma prejudicar nenhum servidor do discord. <br>
> This bot was developed for study purposes and has no intention of invading or in any way harming any discord server. <br>

# 🤖 Instalando e Iniciando o BOT

Caso deseje iniciar o bot em sua máquina local, inicie o arquivo `install.bat` que está na raiz do projeto para instalar todos os módulos necessários. `Certifique-se de ter o NodeJS instalado no seu pc`

Utilize o arquivo `start.bat` para iniciar o bot sem a necessidade do VSCode aberto. Certifique-se de iniciá-lo somente após a instalação de todos os módulos e a configuração de todos os arquivos.

## 💻 Pré-requisitos

Antes de instalar, verifique se sua máquina atende aos seguintes requisitos:

* [Nodejs](https://nodejs.org/en/) v16.9.0 ou superior

# 🔧 Configurando o BOT

Vá para a raiz do projeto e renomeie o arquivo `.env.example` para `.env` e coloque todas as informações necessárias

```bash
ACCOUNT_TOKEN=
# Token da Conta

BOT_TOKEN=
# Token do Bot

GUILD_ID=
# ID do servidor principal (Se deseja utilizar os comandos em mais de um servidor, deixe em branco)

CLIENT_ID=
# ID do bot
```

> [!NOTE]
> Caso deseje usar o bot em mais de um servidor, deixe `GUILD_ID=` em branco. <br>
> Mas, atenção: qualquer atualização nos comandos, podem demorar de minutos até horas para serem atualizados nos servidores. <br>
> Para configurar os comandos em apenas um servidor, configure como `GUILD_ID=IdDoServidor`. <br>

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

Para alterar alguma informação do status do bot, vá para a pasta `events > bot > botReady` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.<br>
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).<br>
`timer:` Tempo em segundos para a troca de mensagens e status.<br>

`online` = status online<br>
`dnd` = status não perturbe<br>
`idle` = status ausente<br>

em `let timer` é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos

## 📂 Comandos

Nome | Categoria | Descrição
| - | - | - |
[/canal](README.md) | Config | Configura, no servidor atual, onde as logs serão enviadas.
[/cargo](README.md) | Config | Define qual é o cargo para poder usar comandos da staff.
[/membros](README.md) | Staff | Retorna a quantidade de membros e servidores sendo monitorados.
[/pesquisar](README.md) | Staff | Pesquisa as informações de um usuário específico.
[/ping](README.md) | Geral | Responde qual é o tempo de resposta do bot.

## 🔒 Pegar token da conta

1. [abra o discord](https://discord.com/app) pelo navegador.
2. Faça login na conta que você deseja pegar o token.
3. Aperte simultâneamente `CTRL + SHIFT + I`.
4. Procure pela opção `Console`.
5. Coloque o seguinte código:

```js
window.webpackChunkdiscord_app.push([
  [Math.random()],
  {},
  req => {
    if (!req.c) return;
    for (const m of Object.keys(req.c)
      .map(x => req.c[x].exports)
      .filter(x => x)) {
      if (m.default && m.default.getToken !== undefined) {
        return copy(m.default.getToken());
      }
      if (m.getToken !== undefined) {
        return copy(m.getToken());
      }
    }
  },
]);
console.log('%cWorked!', 'font-size: 50px');
console.log(`%cYou now have your token in the clipboard!`, 'font-size: 16px');
```

6. Se você tiver feito tudo certo, o token estará copiado na sua área de transferência.