#  🖥️ Desafio Node 1 💻

Esse projeto foi desenvolvido dentro do módulo de Back-end, do DevClub com Rodolfo Mori, curso de FullStack Pró.
Módulo de back-end com o objetivo de ensinar as aplicabilidades básicas de node, como o Node funciona, a utilização das bibliotecas, protocolos HTTP, middlewares, route params, body params.

Principais desafios foi adicionar as rotas e middlewares, pois um dos requisitos de desafio foi utilizar 2 middlewares e a utilização do Cors.

**Sobre o desafio** Criar uma aplicação que fará o cadastro dos pedidos de uma hamburgueria, utilizando o Node e Express. 

![image](./Imagemdoprojeto.png)

## :avocado: Regras do desafio 

Rotas
POST /order: A rota deve receber o pedido do cliente, o nome do cliente e o valor do pedido, essas informações devem ser passadas dentro do corpo(body) da requisição, e com essas informações você deve registrar o novo pedido dentro de um array no seguinte formato: { id: "ac3ebf68-e0ad-4c1d-9822-ff1b849589a8", order: "X- Salada, 2 batatas grandes, 1 coca-cola", clientName:"José", price: 44.50, status:"Em preparação" }. Não se esqueça que o ID deve ser gerado por você, dentro do código utilizando UUID V4, assim que o pedido é criado, você deve sempre colocar o status como "Em preparação".

GET /order: Rota que lista todos os pedidos já feitos.

PUT /order/:id: Essa rota deve alterar um pedido já feito. Pode alterar,um ou todos os dados do pedido.O id do pedido deve ser enviado nos parâmetros da rota.

DELETE /order/:id: Essa rota deve deletar um pedido já feito com o id enviado nos parâmetros da rota.

GET /order/:id: Essa rota recebe o id nos parâmetros e deve retornar um pedido específico.

PATCH /order/:id: Essa rota recebe o id nos parâmetros e assim que ela for chamada, deve alterar o status do pedido recebido pelo id para "Pronto".

Exemplo
Se eu chamar a rota POST /order repassando { order: "X- Salada, 2 batatas grandes, 1 coca-cola", clienteName:"José", price: 44.50 }, o array deve ficar assim:

[
  {
    id: "ac3ebf68-e0ad-4c1d-9822-ff1b849589a8",
    order: "X- Salada, 2 batatas grandes, 1 coca-cola",
    clienteName:"José", 
    price: 44.50,
    status:"Em preparação"
  }
];
Se eu chamar a rota PATCH /order/ac3ebf68-e0ad-4c1d-9822-ff1b849589a8, o array deve ficar assim:

[
  {
    id: "ac3ebf68-e0ad-4c1d-9822-ff1b849589a8",
    order: "X- Salada, 2 batatas grandes, 1 coca-cola",
    clienteName:"José", 
    price: 44.50,
    status:"Pronto"
  }
];
Middlewares
Crie um middleware que será utilizado em todas rotas que recebem o parâmetro ID, então ele deve verificar se o ID passado existe. Se não existir retorne um erro, caso contrário permita a requisição continuar normalmente;

Crie um middleware que é chamado em todas requisições que tenha um console.log que mostra o método da requisiçao(GET,POST,PUT,DELETE, etc) e também a url da requisição.

Exemplo
[GET] - /order


## 🛠️ Construído com

Ferramentas utilizadas para construção do conversor de moedas foram:

![image](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

![image](https://camo.githubusercontent.com/194ae9b0be9bfd4caedab16de320d3987f4c144112461590a206262d21eb769b/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d56697375616c25323053747564696f253230436f64652d3333333333333f7374796c653d666c6174266c6f676f3d76697375616c2d73747564696f2d636f6465266c6f676f436f6c6f723d303037414343)

![image](https://img.shields.io/badge/Insomnia-black?style=for-the-badge&logo=insomnia&logoColor=5849BE)

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)

![NPM](https://img.shields.io/badge/NPM-%23000000.svg?style=for-the-badge&logo=npm&logoColor=white)

![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)

## 🖇️ Colaboradores

<table>
  <tr>
    <td align="right">
      <a href="https://github.com/rodolfomori" target="blank">
        <img src="https://user-images.githubusercontent.com/95030203/155012879-fc6991b4-5357-4675-9ef5-1dd56f795265.png" width="100px;" alt="Foto do Rodolfo Mori"/><br>
        <sub>
          <b>Rodolfo Mori</b>
        </sub>
      </a>
    </td>



  <tr>
    <td align="center">
      <a href="https://github.com/Cibell" target="blank">
        <img src="https://avatars.githubusercontent.com/u/88112866?v=4" width="100px;" alt="Foto da Cibele"/><br>
        <sub>
          <b>Cibele (Cibell)</b>
        </sub>
      </a>
    </td>
    </table>



## ✒️ Autores

- **Autor do projeto Rodolfo Mori** - [Fundador do DevClub](https://github.com/rodolfomori)

  

## 📄 Licença

Este projeto está sob a licença DevClub

## 🎁 Agradecimento todo especial!

Ao meu esposo **Gustavo Machado Quintilhano**, que mesmo sendo de BI ele me apoia e tenta me ajudar no que é possível!

Ao meu irmão [**Bruno Lebrão**](https://github.com/brunolebrao) , meu programador favorito, obrigada por toda a paciência e ajuda!