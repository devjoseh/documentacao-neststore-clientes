# Bem-Vindo(a)
## 👑 _Documentação - Economy System - V14.x_

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

## `bitcoin.js`

Configurações das probabilidades de uma placa de vídeo conseguir minerar bitcoin com sucesso. 
Quanto maior a probabilidade, mais bitcoins serão minerados.

```
module.exports = {
    placas: {
        geforce1030: { probabilidade: 0.002 },
        rx550: { probabilidade: 0.003 },
        gtx1050: { probabilidade: 0.006 },
        rtx2060: { probabilidade: 0.007 },
        rtx3060: { probabilidade: 0.008 },
        rtx4090: { probabilidade: 0.009 }, 
    }
}
```

Nesse arquivo, existem os ids e as probabilidades das placas. Ex: rx550 é o id da placa.

## `economia.js`

Configurações gerais do sistema de economia

`canalLogs:` ID do canal onde algumas logs serão enviadas, esse canal deve ser visível apenas para a staff. <br>
`canalErros:` ID do canal onde algumas logs serão enviadas quando algum erro acontecer com o bot. <br>
`cargoStaff:` ID's dos cargos que vão poder usar os comandos de staff. <br>
`moedaEco:` Nome da moeda que será usada. Ex: Gemas, Kwanzas, Etc. <br>
`cooldownAposta:` Tempo, em segundos, para realizar uma outra aposta com alguém. <br>
`porcentagemTaxa:` Porcentagem de quanto será pegado como taxa das transferências. <br>
`taxaCasamento:` Preço que será pego de cada membro para realizar o casamento. <br>

### Em Bitcoin

`tempoAtualizacaoBitcoin:` Tempo em Ms para o valor do bitcoin ser alterado. <br>
`taxaAleatoriaBitcoin:` Valores que podem vir aleatoriamente para a venda do bitcoin. <br>

### Em level

`xpAleatorioJobDaily:` Quantia de xp aleatorio que ganha trabalhando e no daily. <br>
`xpAleatorioMessage:` Quantia de xp aleatorio que ganha por mensagem enviada. <br>
`xpPerLevel:` Quantia de XP necessária para upar cada level. Ex: 100. <br>
`cooldownMessage:`  Cooldown, em segundos, entre uma mensagem e outra para ganhar xp. <br>

### Em daily

`valorMinimo:` Quantia mínima que pode vir no daily. <br>
`valorMaximo:` Quantia máxima que pode vir no daily. <br>

### Em roleta

`vermelho:` Quantidade que o dinheiro é multiplicado ao cair no vermelho. <br>
`preto:` Quantidade que o dinheiro é multiplicado ao cair no preto. <br>
`verde:` Quantidade que o dinheiro é multiplicado ao cair no verde. <br>
`apostaMinima:` Valor minimo necessário para realizar a aposta. <br>
`apostaMaxima:` Valor máximo que pode ser apostado. <br>

### Em slots

`items:` Itens que serão sorteados no caça-níquel, no caso, os emojis. <br>
`duo:` Quantidade que o dinheiro é multiplicado ao vir um duo. <br>
`trio:` Quantidade que o dinheiro é multiplicado ao vir um trio. <br>
`apostaMinima:` Valor minimo necessário para realizar a aposta. <br>
`apostaMaxima:` Valor máximo que pode ser apostado. <br>
`probabilidades:` Probabilidade de cada item aparecer no caça-níquel. <br>

### Em blackjack

`apostaMinima:` Valor minimo necessário para realizar a aposta. <br>
`apostaMaxima:` Valor máximo que pode ser apostado. <br>

### Em aposta

`apostaMinima:` Valor minimo necessário para realizar a aposta. <br>
`apostaMaxima:` Valor máximo que pode ser apostado. <br>

### Em roubos

`chanceRouboSucesso:` Porcentagem de chance do roubo dar certo. 1 - 100. <br>
`cooldown:` Cooldown, em segundos, para realizar outro roubo. <br>

```
{
porcentagens: {
        Configuração da porcentagem minima e maxima que podem vir para realizar o roubo
        Ex: se vier 10% e o membro roubado tiver 1000$, o assaltante ganhará 100$
        minimo: 5, 
        maximo: 15,
    },
    fianca: {
        Configuração do valor minimo e maximo que podem ser cobrados de fiança caso o assaltante seja pego
        minimo: 200,
        maximo: 700,
    }
}
```

## `itens.js`

Arquivo de configuração onde os itens devem ser configurados:

```
module.exports = {
    loja: {
        mercadoNegro: {
            faca: { nome: "Faca", preco: 500, },
            glock: { nome: "Glock", preco: 3000, },
            ak47: { nome: "AK47", preco: 8000, },
        },
        mineracao: {
            geforce1030: { nome: "GeForce GT 1030", preco: 5000, },
            rx550: { nome: "Radeon RX 550", preco: 8000, },
            gtx1050: { nome: "GeForce GTX 1050 Ti", preco: 11000, },
            rtx2060: { nome: "GeForce RTX 2060", preco: 15000, },
            rtx3060: { nome: "GeForce RTX 3060", preco: 25000, },
            rtx4090: { nome: "GeForce RTX 4090", preco: 35000, },
        },
        diversos: {
            anel: { nome: "Anel", preco: 2500, },
        },
    }
}
```

## Configurando o banco de dados

Vá para a pasta `events > client > firebase.js`
Nesse arquivo é onde deve-se configurar o banco de dados. Segue o tutorial:

1. [Clique aqui](https://firebase.google.com/docs?hl=pt&authuser=0) para acessar o firebase
2. No canto superior direito, clique em `ir para o console`
3. Clique no botão de `adicionar projeto`
4. Coloque o nome do seu server ou qualquer outro
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

# Status do Bot

Vá para a pasta `events > client > ready.js` para configurar o status do bot.

`activities:` Mensagens exibidas no status do bot.<br>
`status:` Status aleatórios que aparecerão no bot (online, não perturbe, ausente).<br>
`timer:` Tempo em segundos para a troca de mensagens e status.<br>

`online` = status online<br>
`dnd` = status não perturbe<br>
`idle` = status ausente<br>

em let timer é o tempo que cada mensagem e status serão trocados, o tempo deve ser configurado em segundos