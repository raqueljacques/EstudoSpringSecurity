# Spring Security Basic Authentication

Este projeto consiste em uma API simples desenvolvida com base em uma aula do canal [Neckel Tech](https://www.youtube.com/watch?v=bnQ5_LmA8wA), com o propósito de aprimorar o conhecimento em autenticação e autorização.
Utilizou-se Java, Java Spring, Mysql como banco de dados, e o Spring Security para controle de autenticação.

## Instalação
1. Clone o repositório.
   ```
   git clone https://github.com/raqueljacques/EstudoSpringSecurity.git
   ```
2. Instale as dependências utilizando o Maven.
3. Instale o MySQL.

## Uso 
1. Execute a aplicação.
2. A API estará acessível em http://localhost:8080.

## Endpoints
A API oferece os seguintes endpoints:

### Usuário
```
POST /user - Cria um novo usuário, podendo ser atribuído papéis.
```

### Produto
```
GET /product - Lista todos os produtos.

POST /product - Cria um novo produto.

PUT /product - Atualiza um produto.

DELETE /product - Deleta um produto.
```

## Autenticação

A autenticação na API é gerenciada pelo Spring Security, onde cada papel representa uma autorização em um endpoint de produto:

```
PRODUCT_SELECT
PRODUCT_INSERT
PRODUCT_UPDATE
PRODUCT_DELETE
```

## Banco de Dados
O projeto utiliza o MySQL, portanto, é necessário configurar o banco no arquivo `application.properties` e adicionar os papéis à tabela `role`.

```sql
INSERT INTO role (NAME) VALUES
("PRODUCT_SELECT"),
("PRODUCT_INSERT"),
("PRODUCT_UPDATE"),
("PRODUCT_DELETE");
```
