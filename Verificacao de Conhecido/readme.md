# Bem-Vindo(a)
## 👑 _Documentação - Verificação de Conhecido - V14.x_

# Configuração Inicial

Caso deseje iniciar o bot em sua máquina local, inicie o arquivo `install.bat` que está na raiz do projeto para instalar todos os módulos necessários. `Certifique-se de ter o NodeJS instalado no seu pc`

Utilize o arquivo `start.bat` para iniciar o bot sem a necessidade do VSCode aberto. Certifique-se de iniciá-lo somente após a instalação de todos os módulos e a configuração de todos os arquivos.

# Arquivos na Pasta "Configs"

## `config.js`

```bash
const config: Config = {
    token: "",
    # O token do seu bot

    guild_id: "",
    # ID do servidor principal do bot
    client_id: "",
    # ID do bot
    owner_id: ""
    # ID do dono do bot
}
```

> [!NOTE]
> Se você configurar o `guild_id` como: `guild_id: null` os comandos serão registrados globalmente.
> Para configurar os comandos em apenas um servidor, configure como `guild_id: "ID DO SERVIDOR"`

## `settings.js`

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

# Status do Bot

Vá para a pasta `events > client > ready.js` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.<br>
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).<br>
`timer:` Tempo em segundos para a troca de mensagens e status.<br>

`online` = status online<br>
`dnd` = status não perturbe<br>
`idle` = status ausente<br>

em let timer é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos