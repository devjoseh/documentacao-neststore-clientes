# Bem-Vindo(a)
## 👑 _Documentação - Register Using Forms & Modals - V14.x_

# Configuração Inicial

Antes de iniciar o bot em sua máquina local, execute npm install no terminal para instalar todos os módulos necessários.

Utilize o arquivo start.bat para iniciar o bot sem a necessidade do VSCode aberto. Certifique-se de iniciá-lo somente após a instalação de todos os módulos e a configuração de todos os arquivos.

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

## `createChannel.js`

Configurações relacionadas a cargos e canais para gerenciamento de comandos e formulários.

`cargosAutorizadosComandos:` Cargos que poderão utilizar todos os comandos.
`cargosCriarCanais:` Cargos que podem usar o sistema de criar canais por formulário.
`cargosSuporte:` Cargos que podem ver os canais criados pelo formulário.
`cargosRegistro:` Cargos que serão adicionados às pessoas que tiverem seus formulários aceitos.
`cargosAnaliseForms:` Cargos que poderão responder os formulários enviados.
`canalErros:` Canal que será enviado as mensagens de erros do bot.
`canalFormulario:` Canal que será enviado as mensagens dos formulários.
`canalParceiros:` Canal que será enviado as mensagens dos formulários de parceiros.
`categoriaCanais:` Categoria onde os canais dos formulários aceitos serão criados.
`canalLogs:` Canal onde as logs de cargos removidos serão enviadas.
`cargosParceiros:` IDs dos cargos que serão adicionados às pessoas que tiverem o formulário de parceiros aprovado.
`formularioNickname:` Texto que será adicionado aos parceiros.
`parceiroNickname:` Texto que será adicionado aos parceiros.

`tituloEmbed:` Título da embed que é enviada pelo comando canalembed.
`mensagemDescricaoEmbed:` Mensagem que fica na descrição da embed que é enviada pelo comando canalembed.
`emojiBotao:` Emoji que fica no botão da embed que é enviada pelo comando canalembed.
`mensagemBotao:` Texto que fica no botão da embed que é enviada pelo comando canalembed.

`tituloFormulario:` Título que aparece no formulário ao clicar no botão.

### Em pergunta1, pergunta2, etc:

`titulo:` Título da pergunta.
`placeholder:` Mensagem que fica no campo do texto.
`maxCarac:` Quantia máxima de caracteres que podem ser digitados.
`minCarac:` Quantia mínima de caracteres que podem ser digitados.

### msgFormularioAprovado e msgFormularioNegado

Mensagens que são enviadas no privado do usuário quando o formulário é aceito ou negado.

### Em msgFormatadaCanal:

`linkImagem:` Link da imagem com .png no final do link (recomendado upar a imagem no imgur).
`textoBoasVindas:` Texto que você pode usar para dar boas-vindas ao usuário, exemplo: Olá! {member}.
`textoDescricao:` Texto que você pode usar para explicar alguma coisa ou só complementar as boas-vindas.
`titulo1:` Texto da pergunta de Nome e ID.
`titulo2:` Texto da pergunta de Tipo de Conteúdo.
`titulo3:` Texto da pergunta de Rede Social.
`titulo4:` Texto da pergunta de Link.

## `embeds.js`

no topo, você verá a configuração "embeds" que é onde você deve colocar o titulo e texto das embeds onde ficam os botões dos formulários 

em botoes, você deve colocar os textos dos botões que aparecem nas embeds onde ficam os botões dos formulários e também os botões das mensagens dos formulários, no caso, de aprovar e negar

## Status do Bot

Vá para a pasta `events > client > ready.js` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).
`timer:` Tempo em segundos para a troca de mensagens e status.

`online` = status online
`dnd` = status não perturbe
`idle` = status ausente

em let timer é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos