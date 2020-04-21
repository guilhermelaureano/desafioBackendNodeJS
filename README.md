# Bootcamp GoStack
###### Aluno: Guilherme Medeiros Laureano
## Desafio 02: Conceitos do Node.js

Nesse desafio, foi desenvolvido uma aplicação para fixar os conceitos Node.js aprendidos no Bootcamp GoStack Rocketseat - Nível 01.
O desenvolvimento se deu a partir de um [template](https://github.com/Rocketseat/gostack-template-conceitos-nodejs) disponibilizado pela Rocketseat.

### Sobre a aplicação
Essa é uma aplicação para armazenar repositórios para um portfólio, que permite a criação (POST), a listagem (GET), a atualização (PUT) e remoção (DELETE) dos repositórios. Além disso, a aplicação permite que os repositórios possam receber (POST) "likes".

### Rotas da aplicação


- POST `/repositories`: A rota deve receber title, url e techs dentro do corpo da requisição, sendo a URL o link para o github desse repositório. Ao cadastrar um novo projeto, ele é armazenado dentro de um objeto no seguinte formato:
```
{
  id: "uuid",
  title: 'Desafio Node.js',
  url: 'https://github.com/guilhermelaureano/desafioBackendNodeJS',
  techs: ["JavaScript", "Node.js"],
  likes: 0
};
```
O ID é gerado atráves do formato UUID (do inglês <i>Universally Unique IDentifier</i>), e os likes são iniciados com valor 0.

- GET `/repositories`: Rota que lista todos os repositórios;

- PUT `/repositories/:id`: A rota possibilita alterar apenas o title, a url e as techs do repositório que possua o id igual ao id presente nos parâmetros da rota;

- DELETE `/repositories/:id`: A rota remove o repositório com o id presente nos parâmetros da rota;

- POST `/repositories/:id/like`: A rota aumenta o número de likes do repositório específico escolhido através do id presente nos parâmetros da rota, a cada chamada dessa rota, o número de likes é aumentado em 1;


