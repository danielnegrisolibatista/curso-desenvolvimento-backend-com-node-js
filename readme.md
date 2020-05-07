# Curso Desenvolvimento backend com Node.js

- Autor: Gianfranco Meneguz
- Origem: Digital Innovation One

## Módulo I - Desenvolvimento de Node.js com banco de dados PostgreSQL

### Aula I - O que é e como trabalhar com PostgreSQL

#### Prática - Aula I - O que é e como trabalhar com PostgreSQL

- Instalar o [Node.js](https://nodejs.org/en/download/)
- Instalar o Banco de dados [PostgreSQL](https://www.postgresql.org/download/)
- Clonar o [repositório](https://github.com/gmeneguz/intro_node_pg_sequelize.git)
  - `git clone https://github.com/gmeneguz/intro_node_pg_sequelize.git`
- Realizar checkout da branch passo1
  - `git checkout passo1`
- Executar os scripts sql da pasta `intro_node_pg_sequelize/sql` no seu Postgres

### Aula II - Utilizando Node.js com PostgreSQL

#### Prática - Aula II - Utilizando Node.js com PostgreSQL

- Realizar checkout da branch passo2
  - `git checkout passo2`
- Instalar as dependências
  - `npm install`
- Executar os scripts js da pasta `intro_node_pg_sequelize/js`
  - `node js/1_drop.js`
  - `node js/2_create.js`
  - `node js/3_insert.js`
  - `node js/4_select.js`

- Exercício complementar para prática:
  - Crie o update `js/5_update.js`
  - Crie o delete `js/6_delete.js`

### Aula III - Introdução a ORMs e Sequelize

#### ORM

É um framework que ajuda no mapeamento de objetos com os elementos do banco de dados.

Alguns exemplos:

- Hibernate (Java)
- EntityFramework (.NET)
- DataMapper (Ruby)
- Sequelize (Node)

#### Sequelize

- Compatível com os bancos de dados
  - MySQL
  - Sqlite
  - PostgreSQL
  - SQL Server
- Versátil
- Robusto

#### Prática - Aula III - Introdução a ORMs e Sequelize

- Realizar checkout da branch passo3
  - `git checkout passo3`
- Instalar as dependências
  - `npm install`
- Verificar os scripts js de criação de modelos na pasta `intro_node_pg_sequelize/sequelize/models`
- Executar os scripts js da pasta `intro_node_pg_sequelize/sequelize`
  - `node sequelize/1_create.js`
  - `node sequelize/2_insert.js`
  - `node sequelize/3_select.js`
  - `node sequelize/4_select_advanced.js`
- Exercício complementar para prática:
  - Adicione o campo data no evento
  - Cadastre 5 eventos com data futura
  - Liste os eventos que tenham a data no mês de abril

#### Exerícios - Módulo I - Desenvolvimento de Node.js com banco de dados PostgreSQL

Qual dos tipos de dados abaixo NÃO é utilizado no banco de dados Postgresql:

- Image

Ao utilizar Sequelize em Node.js, o que seriam Scopes?

- São queries ou consultas pré definidas que podem ser utilizadas posteriormente.

Sobre ORMs (Mapeamento Objeto-Relacional), marque a alternativa VERDADEIRA:

- Tem objetivo de facilitar o desenvolvimento e manutenção dos aplicativos que utilizam banco de dados.

No Sequelize, hooks são:

- Gatilhos executados antes ou depois de alguma ação ser executada pelo Sequelize.

Referente a ORMs (Mapeamento Objeto-Relacional), quais definições podem ser aplicadas ao termo migrations do banco de dados?

I) São configurações para alterar ou restaurar a estrutura, principalmente tabelas e colunas,  do banco de dados.

II) São configurações de backup dos dados presentes no banco de dados

III) São configurações de queries para buscar certo tipo de dados no banco.

IV) São Operadores do tipo AND, OR e BETWEEN.

V) São utilizados para alterar a estrutura do banco de dados de um estado atual para outro estado posterior ou anterior.

- I e V.

Considerando que model é um modelo do ORM Sequelize em Node.js, qual dos comandos abaixo abaixo criaria um novo item no banco de dados?

- `model.create({nome: "Evento"})`

Em qual situação abaixo seria necessário utilizar uma transação no banco de dados?

- Quando queremos garantir que diversos comandos sejam executados sem falha. Se algum deles falhar, todos comandos devem ser cancelados.

Quais dos tipos de banco de dados abaixo NÃO é um banco de dados relacional?

- MongoDb.

Quais dos comandos abaixo NÃO é um comando SQL?

- `GENERATE.`

Ao montarmos uma query parametrizada com o módulo em node.js, qual é a sintaxe correta para que os campos nome e e-mail sejam substituídos corretamente?

- `"INSERT INTO (nome, email) VALUES ($1,$2)"`

## Módulo II - Desenvolvimento de Node.js com banco de dados MongoDB

### Aula I - SQL vs NoSQL

### Aula II - O que é o MongoDB

### Aula II - Pratique os conceitos aprendidos

## Módulo III - Criando serviços escaláveis com Hapi

### Aula I - Aprenda sobre o framework Hapi

### Aula II - Desenvolvendo códigos com Hapi

## Módulo IV - Desenvolvendo aplicações seguras com JWT

### Aula I - O que é JWT

## Módulo V - Conceitos aplicados a qualidade de código e automação de testes

### Aula I - O que é qualidade

### Aula II - Ferramentas de Lint

### Aula III - Desenvolvimento guiado por testes

## Módulo VI - Implementando um servidor WebSocket com o Node.js

### Aula I - O que é e como funciona o WebSocket

### Aula II - Aprenda a desenvolver WebSocket na prática
