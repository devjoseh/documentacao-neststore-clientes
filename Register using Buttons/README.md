# Bem-Vindo(a)
## 👑 _Documentação - Register using Buttons - V14.x_

# Configuração Inicial

Caso deseje iniciar o bot em sua máquina local, digite `npm install` no terminal para instalar todos os módulos necessários.

Utilize o arquivo `start.bat` para iniciar o bot sem a necessidade do VSCode aberto. Certifique-se de iniciá-lo somente após a instalação de todos os módulos e a configuração de todos os arquivos.

# Arquivos na Pasta "Configs"

## `config.json`

```
{
  "token": "Token do bot",
  "prefix": "Prefixo usado para comandos com message commands",
  "guild_id": "ID do servidor principal onde o bot deve funcionar",
  "client_id": "ID do bot",
  "owner_id": "ID do proprietário do bot (seu ID)"
}
```

## `settings.json`

```
{
  "color": "Cor de todas as embeds enviadas pelo bot (usando o formato hex)",
  "titulo": "Título das embeds",
  "footer": "Rodapé das embeds",
  "prefix": "O mesmo prefixo configurado no arquivo config.json"
}
```

## `formularios.js`

Configurações relacionadas a todo o sistema de registro

`imgEmbed:` Imagem que será colocada nas embeds de setagem e removersetagem. <br>

`canalErros:` ID do canal onde os erros que acontecerem com o bot serão enviados.<br>
`canalLogsSetagem:` ID do canal onde serão enviados as logs das setagens realizadas.<br>
`canalLogsRemoverSetagem:` ID do canal onde serão enviados as logs das setagens removidas.<br>

`cargoStaff:` ID do cargo que pode usar os comandos de setagem e removersetagem.<br>

## em opcoes

`cargo:` ID do cargo ou dos cargos que serão adicionados para aquela opcao.<br>
`emoji:` Emoji que aparecerá na embed e no nickname dos usuários.<br>
`texto:` Texto que aparecerá na embed.<br>

## Status do Bot

Vá para a pasta `events > client > ready.js` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.<br>
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).<br>
`timer:` Tempo em segundos para a troca de mensagens e status.<br>

`online` = status online<br>
`dnd` = status não perturbe<br>
`idle` = status ausente<br>

em let timer é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos