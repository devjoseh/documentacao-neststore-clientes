# Bem-Vindo(a)
## 👑 _Documentação - Register Using Forms & Modals - V14.x_

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

## `createChannel.js`

Configurações relacionadas a cargos e canais para gerenciamento de comandos e formulários.

`cargosAutorizadosComandos:` Cargos que poderão utilizar todos os comandos. <br>
`cargosCriarCanais:` Cargos que podem usar o sistema de criar canais por formulário. <br>
`cargosSuporte:` Cargos que podem ver os canais criados pelo formulário. <br>
`cargosRegistro:` Cargos que serão adicionados às pessoas que tiverem seus formulários aceitos. <br>
`cargosAnaliseForms:` Cargos que poderão responder os formulários enviados. <br>
`canalErros:` Canal que será enviado as mensagens de erros do bot. <br>
`canalFormulario:` Canal que será enviado as mensagens dos formulários. <br>
`canalParceiros:` Canal que será enviado as mensagens dos formulários de parceiros. <br>
`categoriaCanais:` Categoria onde os canais dos formulários aceitos serão criados. <br>
`canalLogs:` Canal onde as logs de cargos removidos serão enviadas. <br>
`cargosParceiros:` IDs dos cargos que serão adicionados às pessoas que tiverem o formulário de parceiros aprovado. <br>
`formularioNickname:` Texto que será adicionado aos parceiros. <br>
`parceiroNickname:` Texto que será adicionado aos parceiros. <br>

`tituloEmbed:` Título da embed que é enviada pelo comando canalembed.<br>
`mensagemDescricaoEmbed:` Mensagem que fica na descrição da embed que é enviada pelo comando canalembed.<br>
`emojiBotao:` Emoji que fica no botão da embed que é enviada pelo comando canalembed.<br>
`mensagemBotao:` Texto que fica no botão da embed que é enviada pelo comando canalembed.<br>

`tituloFormulario:` Título que aparece no formulário ao clicar no botão.

### Em pergunta1, pergunta2, etc:

`titulo:` Título da pergunta. <br>
`placeholder:` Mensagem que fica no campo do texto. <br>
`maxCarac:` Quantia máxima de caracteres que podem ser digitados. <br>
`minCarac:` Quantia mínima de caracteres que devem ser digitados. <br>

### msgFormularioAprovado e msgFormularioNegado

Mensagens que são enviadas no privado do usuário quando o formulário é aceito ou negado.

### Em msgFormatadaCanal:

`linkImagem:` Link da imagem com .png no final do link (recomendado upar a imagem no imgur).<br>
`textoBoasVindas:` Texto que você pode usar para dar boas-vindas ao usuário, exemplo: Olá! {member}.<br>
`textoDescricao:` Texto que você pode usar para explicar alguma coisa ou só complementar as boas-vindas.<br>
`titulo1:` Texto da pergunta de Nome e ID.<br>
`titulo2:` Texto da pergunta de Tipo de Conteúdo.<br>
`titulo3:` Texto da pergunta de Rede Social.<br>
`titulo4:` Texto da pergunta de Link.<br>

## `embeds.js`

no topo, você verá a configuração "embeds" que é onde você deve colocar o titulo e texto das embeds onde ficam os botões dos formulários 

em botoes, você deve colocar os textos dos botões que aparecem nas embeds onde ficam os botões dos formulários e também os botões das mensagens dos formulários, no caso, de aprovar e negar

# Status do Bot

Vá para a pasta `events > client > ready.js` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.<br>
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).<br>
`timer:` Tempo em segundos para a troca de mensagens e status.<br>

`online` = status online<br>
`dnd` = status não perturbe<br>
`idle` = status ausente<br>

em let timer é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos