# Hamburgueria-2-0-server

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth, desenvolvido com propósito educacional.

## Endpoints

A API tem um total de 4 endpoints.
A URL base da API é https://hamburgueria-2-0-server.herokuapp.com

### Usuarios:

Dentre os endpoints 2 são utilizados para a gestão de usuários:

#### Cadastro

Cadastrar Usuario.

POST /users

Exemplo de Body para a requisição:

```JSON
    {
        "name": "string",
        "email": "string",
        "password": "string",
    }
```

#### Login

Efetuar Login.

POST /login

Exemplo de Body para a requisição:

```JSON
    {
        "email": "string",
        "password": "string",
    }
```

### Produtos:

Pegar a lista de produtos disponível.

GET /products

Essa requisição não precisa de autorização e body.

### Pedidos:

Enviar o pedido.

POST /orders:
Essa requisição precisa de autorização com token.

```JSON
    {
        "userId": "number",
        "orderTime": "string",
        "order": [
            {
                "id": "number",
                "name": "string",
                "category": "string",
                "price": "number",
                "image": "string",
                "amount": "number",
            },
            {
                "id": "number",
                "name": "string",
                "category": "string",
                "price": "number",
                "image": "string",
                "amount": "number",
            }
        ],
    }
```
