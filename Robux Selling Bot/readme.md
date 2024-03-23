# Bem-Vindo(a)
## 👑 _Documentação - Robux Selling Bot - V14.x_

# Configuração Inicial

Caso deseje iniciar o bot em sua máquina local, inicie o arquivo `install.bat` que está na raiz do projeto para instalar todos os módulos necessários. `Certifique-se de ter o NodeJS instalado no seu pc`

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

## `embeds.js`

Todas as configurações das embeds enviadas pelo bot. Arquivo já configurado, mas pode ser alterado como desejar.

## `messages.js`

Todas as configurações dos emojis usados pelo bot. Arquivo já configurado, mas pode ser alterado como desejar.

## `paymentConfig.js`

`email:` Email do pix cadastrado no mercadopago. <br>
`nome:` Primeiro nome do titular da conta. <br>
`sobrenome:` Sobrenome do titular da conta. <br>
`cpf:` CPF do titular da conta. <br>

### Em endereco:

`cep:` CEP do titular da conta. <br>
`rua:` Rua do titular da conta. <br>
`numero:` Numero da casa do titular da conta. <br>
`bairro:` Nome do bairro do titular da conta. <br>
`cidade:` Cidade do bairro do titular da conta. <br>
`estado:` Estado do titular da conta. <br>

## `store.js`

Configurações relacionadas a todo o sistema da loja.

`access_token:` Token de acesso da sua conta do Mercado Pago (Credencial). <br>
`cargoCliente` Cargo que será adicinado a pessoa quando concluir o pagamento de algum produto.

### Em canais:

`logs` Canal onde as logs gerais serão enviadas (criação de produto, etc)
`entregasStaff` Canal onde as logs de compras serão enviadas (log da staff)
`entregasMembros` Canal onde as logs de compras serão enviadas (log que os membros podem ver)
`erros` Canal que serão enviados os erros que acontecerem com o bot
`avaliacoes` Canal onde os clientes podem avaliar a loja com suas próprias palavras
`duvidasFrequentes` Canal onde fica as informações da loja, o canal de Duvidas Frequentes
`logsAcoes` Canal onde as ações como criação de canal, confirmacao de pagamento, etc. serão enviados
`ticket` Canal onde fica a embed que os membros abrem os tickets

### Em atendimento:

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

### Em tickets:

`cargosStaff` Cargos que podem ver todos os tickets abertos naquela categoria
`categoria` Categoria em que os canais serão abertos

### Em compras:

### Robux:

`categoria` ID da categoria em que os carrinhos de robux serão abertos
`cargosStaff` ID de todos os cargos que podem ver os carrinhos abertos naquela categoria
`valor` Se refere a 1000, ou seja, se o valor for 28, 1000 robux = 28.0R$
`minimo`  Valor mínimo de robux que podem ser comprados por carrinho 
`maximo` Valor máximo de robux que podem ser comprados por carrinho

### Gamepass

`categoria` ID da categoria em que os carrinhos de gamepass serão abertos
`cargosStaff` ID de todos os cargos que podem ver os carrinhos abertos naquela categoria
`valor` Se refere a 1000, ou seja, se o valor for 35, 1000 robux = 35.0R$
`maximoGamepass` Quantia máxima de gamepasses que podem ser comprados por carrinho
`minimo` Valor mínimo que as gamepasses devem ter no total
`maximo`Valor máximo que as gamepasses devem ter no total

## Configurando o banco de dados

Vá para a pasta `events > client > firebase.js`
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

21. No bot, vá para: `events > client > firebase` e substitua o código `firebaseConfig` por esse que você copiou
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

# Status do Bot

Vá para a pasta `events > client > ready.js` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.<br>
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).<br>
`timer:` Tempo em segundos para a troca de mensagens e status.<br>

`online` = status online<br>
`dnd` = status não perturbe<br>
`idle` = status ausente<br>

em let timer é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos