# Bem-Vindo(a)
## 👑 _Documentação - Automatic Sell Bot - V14.x_

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

## `store.js`

Configurações relacionadas ao sistema de criação do pagamento e algumas outras configurações

`access_token:` Token de acesso da sua conta do Mercado Pago (Credencial). Veja como configurar abaixo. <br>
`cargosStaff:` Cargos que podem visualizar os carrinhos criados. <br>
`cargoCliente:` Cargo que será adicionado a um membro quando finalizar uma compra. <br>
`cargoWelcome:` Cargo que será adicionado a alguém quando entrar no servidor. <br>
`canalWelcome:` Canal onde as mensagens de entrada serão enviadas. <br>
`canalVoz:` Canal de voz onde o bot irá entrar quando for ligado. <br>
`canalLogs:` Canal que serão enviadas logs normais como a criação de produtos e outros. <br>
`canalEntregaStaff:` Canal onde serão enviadas todas as logs de compras finalizadas apenas para a staff. <br>
`canalEntregaProdutos:` Canal onde serão enviadas as logs de compras finalizadas, essa é a log que os membros comuns podem ver. <br>
`canalErros:` Canal onde serão enviados todos os erros que acontecerem com o bot. <br>
`categoriaCompras:` Categoria onde os carrinhos de compra serão abertos. <br>

## `messages.js`

Configurações relacionadas a formatação das mensagens e embed (botões, textos, etc)

`seta:` Seta que é usada em alguns comandos para estilizar a mensagem e deixa-la bonita, você pode alterar para um -. <br>
`embedImage:` Imagem que será colocada nas embeds de produtos. <br>

### Em buttons

`emojiConfirmar:` Emoji utilizado para estilizar botões de confirmação <br>
`emojiNegar:` Emoji utilizado para estilizar botões de negar <br>

### Em compra

`emojiEmbedCarrinho:` Emoji que fica no botão de compra dos produtos, a embed que o usuário cria o carrinho. <br>
`emojiPix:` Emoji do botão de pix, onde o usuário clica para criar o pagamento. <br>
`emojiCancelar:` Emoji do botão de cancelar, onde o usuário usa para cancelar a compra. <br>
`emojiEnviarQRCode:` Emoji do botão de qrcode, onde o usuário usa para receber o código de qrcode. <br>
`emojiAdicionarProduto:` Emoji do botão de adicionar produto, onde o usuário usa para adicionar mais um produto. <br>
`emojiRemoverProduto:` Emoji do botão de remover produto, onde o usuário usa para remover um produto. <br>
`emojiComprarProduto:` Emoji do botão de compra, onde o usuário usa para iniciar o pagamento. <br>

### Welcome

`mensagem:` Mensagem que é enviada quando um usuário entra no servidor. <br>

## Status do Bot

Vá para a pasta `events > client > ready.js` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.<br>
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).<br>
`timer:` Tempo em segundos para a troca de mensagens e status.<br>

`online` = status online<br>
`dnd` = status não perturbe<br>
`idle` = status ausente<br>

em let timer é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos