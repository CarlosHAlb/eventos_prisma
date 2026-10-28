# Eventos Climáticos

## Sobre o projeto

O projeto **Eventos Climáticos** tem como finalidade permitir o registro e o gerenciamento de eventos climáticos, reunindo informações como cidade, categoria do evento, temperatura máxima, data de ocorrência e impactos gerados.

A aplicação conta com uma interface web conectada a uma API, responsável por realizar a comunicação com o banco de dados e garantir o armazenamento e a consulta dos registros.

## Funcionalidades

- Autenticação de usuários por meio de login.
- Identificação do usuário conectado.
- Registro de novos eventos climáticos.
- Exibição dos eventos armazenados no sistema.
- Consulta dos dados dos eventos cadastrados.
- Alteração das informações de registros existentes.
- Remoção de eventos cadastrados.
- Sugestão automática da descrição do impacto de acordo com o tipo de evento escolhido.
- Armazenamento das informações em um banco de dados MySQL.

## Tecnologias utilizadas

### Front-end
- HTML5
- CSS3
- JavaScript

### Back-end
- Node.js
- Express
- Prisma ORM

### Banco de dados
- MySQL

### Ferramentas de desenvolvimento
- Visual Studio Code
- Git
- GitHub
- Postman

## Telas do sistema

### 1. Página inicial

Apresenta a tela principal da aplicação, identifica o usuário autenticado e disponibiliza acesso às funcionalidades de cadastro e consulta dos eventos climáticos.

![Página inicial do sistema](./assets/home.png)

### 2. Tabela de eventos

Permite visualizar os eventos climáticos cadastrados de maneira organizada, facilitando a consulta das informações disponíveis.

![Tabela de eventos climáticos](./assets/tabela.png)

### 3. Registros cadastrados

Exibe os detalhes dos eventos registrados, incluindo cidade, categoria, temperatura máxima, data e descrição dos impactos. A tela também oferece opções para atualizar ou remover registros.

![Lista de registros cadastrados](./assets/registros.png)

## Estrutura do projeto

```text
eventos/
├── api/
│   ├── src/
│   │   ├── controllers/
│   │   ├── routes/
│   │   └── data/
│   ├── prisma/
│   ├── package.json
│   └── server.js
│
├── web/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   ├── login.js
│   │   └── home.js
│   ├── index.html
│   └── home.html
│
├── screenshots/
│   ├── home.png
│   ├── tabela.png
│   └── registros.png
│
└── README.md
```

## Como executar o projeto

### 1. Pré-requisitos

Antes de iniciar, verifique se as seguintes ferramentas estão instaladas:

- Node.js
- MySQL
- Visual Studio Code
- Git

### 2. Instalar as dependências

Abra o terminal na pasta `api` do projeto e execute:

```bash
cd api
npm install
```

Configure as variáveis de ambiente e os dados de conexão com o MySQL conforme as definições utilizadas na aplicação.

Caso necessário, execute as migrações do Prisma e gere o cliente do ORM de acordo com a configuração do projeto.

### 3. Executar a API

Na pasta `api`, inicie o servidor utilizando o comando configurado no projeto. Se o arquivo principal for `server.js`, execute:

```bash
node server.js
```

Por padrão, a API estará disponível no endereço:

```text
http://localhost:3000
```

### 4. Iniciar o front-end

Abra o arquivo `web/index.html` utilizando a extensão Live Server do Visual Studio Code.

Com a API em execução, acesse a tela de login e utilize uma conta previamente cadastrada no banco de dados para entrar no sistema.

## Principais rotas da API

| Método HTTP | Rota | Funcionalidade |
|---|---|---|
| POST | `/usuario/login` | Autenticar usuário |
| POST | `/usuario` | Cadastrar usuário |
| GET | `/usuario` | Listar usuários |
| GET | `/usuario/:id` | Consultar usuário por identificador |
| PUT | `/usuario/:id` | Atualizar usuário |
| DELETE | `/usuario/:id` | Excluir usuário |
| POST | `/evento` | Cadastrar evento climático |
| GET | `/evento` | Listar eventos cadastrados |
| PUT | `/evento/:id` | Atualizar evento |
| DELETE | `/evento/:id` | Excluir evento |

## Banco de dados

O MySQL é utilizado para armazenar os dados dos usuários e os registros dos eventos climáticos. A integração entre a API e o banco é realizada com o auxílio do Prisma ORM.

Cada evento pode conter as seguintes informações:

- Cidade onde ocorreu.
- Tipo de evento climático.
- Temperatura máxima registrada.
- Data de ocorrência.
- Descrição dos impactos.
- Identificação do usuário relacionado ao cadastro.

## Objetivo educacional

O desenvolvimento deste projeto permite aplicar conhecimentos de programação web, integração entre front-end e back-end, criação de APIs REST, operações CRUD e manipulação de bancos de dados relacionais.

A atividade contribui para a compreensão das etapas de desenvolvimento de uma aplicação, desde a organização dos arquivos até a implementação e utilização das funcionalidades.

---
