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

- Existem várias comparações de desempenho realizadas entre NoSQL e o SQL
- A velocidade geralmente é o fator mais importante na decisão de qual banco utilizar
- Há muitas opçoes de banco de dados NoSQL com diferentes funcionalidades que pode ser muito úteis

#### SQL

- SQL é a sigla para *Structured Query Language* (Linguagem de Consulta Estruturada)
- É uma linguagem de consulta a banco de dados relacionais
- Executa comandos para criar, consultar, atualizar e excluir informações no seu banco de dados (CRUD)
- Segue uma modelagem relacional, pelo fato de que todos os dados são guardados em tabelas

#### NoSQL

- NoSQL e a sigla para *Not Only SQL* (Não Apens SQL)
- É o termo utilizado para banco de dados não relacionais de alto desempenho, onde geralmente não é utilizado o SQL como linguagem de consulta
- Criado para ter uma performance melhor e uma escalabilidade mais horizontal

##### Tipos de Banco de dados NoSQL

###### Documentos

- Dados são armazenados como documentos
- Podem ser decritos como dados no formato de chave-valor, como o padrão JSON
- Exemplo: MongoDB

###### Colunas

- Dados são armazenados em linhas particulares de tabela no disco
- Suporta várias linhas e colunas, bem como sub-colunas
- Exemplo: Cassandra

###### Grafos

- Dados são armazenados na forma de grafos (vértices e aresta)
- Exemplo: Neo4j

###### Chave-valor

- Suporta mais carga de dados
- O conceito é que um determinado valor seja acessado através de uma chave identificadora única
- Exemplo: Riak

#### Diferenças entre NoSQL e SQL

| SQL | NoSQL |
| ------ | ------ |
| SQL se baseia no fato de que todos os dados sejam guardados em tabelas | NoSQL não se aplica o conceito de schema: uma chave de valor é que é utilizado para recuperar valores, conjuto de colunas ou documentos |
| SQL você precisa ter o relacionamento entre várias tabelas para ter a informação (entidade e relacionamento) | NoSQL agrupa toda a informação e guarda no mesmo registro |
| SQL term certa dificuldade em conciliar a demanda por escalabilidade | NoSQL deve se levar em consideração a modelagem do sistema |
| SQL tem como ponto forte à consistência das informações | NoSQL garante o último valor atualizado, se não for realizada nenhuma atualização antes da consulta |
|Quanto à segurança está suscetível a ataques|Quanto à segurança está suscetível a ataques|

| SQL Terms / Concepts | MongoDB Terms / Concepts |
| ------ | ------ |
| database | database |
| tables | collections |
| rows | documents (BSON) |
| columns | fields |

- O NoSQL tem muitas vantagens para ser utilizado, mas não é preciso utilizá-lo em todas as situações
- Em muitos sistemas, você pode (e até deve) usar o modelo relacional (SQL)
- O NoSQL é mais indicado para aqueles sistemas que tenham necessidades maiores de armazenamento e desempenho
- O mais comum é usar uma arquitetura híbrida, aproveitando o melhor dos dois modelos

### Aula II - O que é o MongoDB

- Banco de dados orientado a documentos (document-based) no formato JSON
- É o mais usado no mercado
- Não possui como restrição a necessidade de ter as tabelas e colunas criadas previamente
- É possível armazenar registros sem se preocupar com a estrutura de dados (números de campos, tipos, etc)
- Guarda dados em documentos ao invés de tabelas
- Os documentos são agrupados em collections
- Um conjunto de collections forma um banco de dados

#### Recursos do MongoDB

- Sharding: usado para dividir os dados de uma collection entre mais de um servidor
- Capped colletions: collectios com tamanhos predefinidos e com conteúdo rotativo

#### Mongoose

- Solução baseada em esquemas para modelar os dados de uma aplicação
- Possui sistema de conversão de tipos, validação, criação de consultas e hooks para lógica de negócios
- Fornece um mapeamento de objetos do MongoDB similar ao ORM (Object Relational Mapping), conhecido como ODM (Object Data Mapping)
- Traduz os dados do banco de dados para objetos Javascript para serem utilizados pela aplicação

### Aula III - Pratique os conceitos aprendidos

- Criar uma rota na API para "/posts"
- Criar um schema usando Mongoose com os campos:
  - titles (String)
  - content (String)
  - author (String)
  - publishDate (String)
- Implementar os endpoints para cada operação no banco de dados (CRUD)

#### Exerícios - Módulo II - Desenvolvimento de Node.js com banco de dados MongoDB

O que é o MongoDB?

- Banco de dados orientado a documentos (document-based) no formato JSON.

Entre as diferenças entre NoSQL e SQL:

I - O SQL tem certa dificuldade em conciliar a demanda por escalabilidade.

II - Um ponto forte do SQL é quanto à consistência das informações.

III - NoSQL é mais seguro do que o SQL.

- Apenas I e II estão corretas.

Em relação ao Mongoose:

I - Solução baseada em esquemas para modelar os dados de uma aplicação.

II - Possui sistema de conversão de tipos, validação, criação de consultas e hooks para lógica de negócios.

III - Fornece um mapeamento de objetos do MongoDB conhecido como ODM (Object Data Mapping).

- I, II e III estão corretas.

O que é um ODM (Object Data Mapping)?

- erramenta para traduzir os dados do banco de dados para objetos JavaScript para serem utilizados pela aplicação.

São exemplos de bancos de dados não-relacionais:

- MongoDB, Cassandra, Neo4j e Riak.

Em relação ao MongoDB:

I - Guarda dados em tabelas ao invés de documentos.

II - Os documentos são agrupados em collections.

III - É possível armazenar registros sem se preocupar com a estrutura de dados.

- Apenas II e III estão corretas

São tipos de bancos de dados NoSQL:

- Documento, Colunas, Grafos e Chave-valor.

Entre os recursos disponíveis no MongoDB, podemos considerar:

- Capped colletions: collectios com tamanhos predefinidos e com conteúdo rotativo

Qual é o método usado no Mongoose para se conectar ao banco de dados?

- mongoose.connect()

O que é o NoSQL?

- Termo utilizado para banco de dados não relacionais de alto desempenho.

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
