# Bem-Vindo(a)
## 👑 _Documentação - Ticket System with Transcript - V14.x.x_

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

### Em categoriasTicket

Existem 4 categorias (categoria1 - 4), em cada categoria, deve-se colocar o nome do que ela representa. Ex:
categoria1: Suporte
categoria2: Denuncias
categoria3: Compras
categoria4: Report Bugs

### Em emojisEmbedsTickets

São os emojis que ficam nos botões de cada categoria. Cada campo corresponde a uma categoria de cima para baixo (da 1 a 4). Você pode utilizar emojis padrões (apenas o emoji, não pode ser, por exemplo: `:one:` ou `:moneybag:` aperte Windows + . para ver a lista de emojis padrões), emojis não animados do discord <:nomeEmoji:idEmoji> ou emojis animados <a:nomeEmoji:idEmoji>

### Em emojisTickets

São os emojis que aparecerão nas mensagens dentro dos tickets. Você pode colocar qualquer um que quiser, desde que o emoji esteja em algum servidor que o bot está.

## `ticketConfig.js`

No começo do arquivo existem 4 variaveis. Cada variavel corresponde a uma categoria, de cima pra baixo (1 a 4)
Essas 4 variaveis significam quais cargos são permitidos de gerenciar o ticket de cada categoria, podem ser ID's diferentes ou todos os ID's iguais. Para adicionar mais de 1 ID por categoria, siga o formato: 
Exemplo: `cargosCategoria1: ["ID_1", "ID_2", "ID_3"]`

`categories:` Existe 4 campos onde cada campo corresponde a 1 categoria. Deve-se colocar o id da categoria onde os canais serão abertos

`ticketsOpenCategory:` Id da categoria do discord que todos os tickets serão abertos
`ticketsTranscripts:` Id do canal que todos os transcripts serão enviados

`mensagensTickets:` Existem 4 variaveis, cada variavel corresponde a mensagem que é enviada na embed dos tickets abertos. Cada variavel significa uma categoria de cima para baixo (1 a 4)

`descricaoEmbedsCategorias:` São as mensagens enviadas nas embeds que os usuários clicam nos botões. A variavel `descricao` é o texto de horários de atendimento e um aviso, você pode alterar o texto como quiser.
Logo abaixo, estão 4 campos que são uma breve explicação de cada categoria. Exemplo:

A categoria 1 está configurada como Suporte, então a mensagem pode ser:

"Suporte relacionado a problemas encontrados no servidor"

## Status do Bot

Vá para a pasta `events > client > ready.js` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.<br>
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).<br>
`timer:` Tempo em segundos para a troca de mensagens e status.<br>

`online` = status online<br>
`dnd` = status não perturbe<br>
`idle` = status ausente<br>

em let timer é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos