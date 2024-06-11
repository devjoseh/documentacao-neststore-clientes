# Bem-Vindo(a)
## 👑 _Documentação - Verificação de Conhecido - V14.x_

# Configuração Inicial

Caso deseje iniciar o bot em sua máquina local, inicie o arquivo `install.bat` que está na raiz do projeto para instalar todos os módulos necessários. `Certifique-se de ter o NodeJS instalado no seu pc`

Utilize o arquivo `start.bat` para iniciar o bot sem a necessidade do VSCode aberto. Certifique-se de iniciá-lo somente após a instalação de todos os módulos e a configuração de todos os arquivos.

# Arquivos na Pasta "Configs"

## `config.js`

```
{
  "token": "Token do bot",
  "prefix": "Prefixo usado para comandos com message commands",
  "guild_id": "ID do servidor principal onde o bot deve funcionar",
  "client_id": "ID do bot",
  "owner_id": "ID do proprietário do bot (seu ID)"
}
```

## `settings.js`

```
{
  "color": "Cor de todas as embeds enviadas pelo bot (usando o formato hex)",
  "titulo": "Título das embeds",
  "footer": "Rodapé das embeds",
  "prefix": "O mesmo prefixo configurado no arquivo config.json"
}
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