# Documentação do ProjApiControleEstoque

Esta API é uma aplicação desenvolvida com o framework .NET Core 6 e segue os conceitos de Domain Driven Design (DDD), com o objetivo de permitir a gestão de estoque de produtos cadastrados no sistema. O DDD é uma abordagem de desenvolvimento de software que busca modelar o domínio do negócio de forma clara e expressiva, facilitando a evolução e manutenção da aplicação. Através das API's de Produtos e Categorias, é possível realizar operações como cadastro, atualização, exclusão e consulta de usuários (C.R.U.D.), por meio de endpoints HTTP bem definidos e com respostas padronizadas.

## Documentação em Desenvolvimento
## Produtos
### Endpoints

* **GET /produtos**

    Retorna uma lista de todos os produtos cadastrados no sistema.


* **GET /produtos/{id}**

    Retorna um produto específico pelo ID.

* **POST /produtos**

    Cria um novo produto com as informações fornecidas.

* **PUT /produtos/{id}**

    Atualiza um produto específico pelo ID.

* **DELETE /produtos/{id}**

    Exclui um produto específico pelo ID.

### Retornos

* **GET /produtos**

    Retorna uma lista de objetos de produto no seguinte formato:

    ```json
        [
            {
                "id": 1,
                "name": "Produto 1",
                "category": "Category 1",
                "createdAt": "2022-03-01T10:00:00Z",
                "updatedAt": "2022-03-01T10:00:00Z"
            },
            {
                "id": 2,
                "name": "Produto 2",
                "category": "Category 2",
                "createdAt": "2022-03-01T10:00:00Z",
                "updatedAt": "2022-03-01T10:00:00Z"
            }
        ]
    ```

* **GET /produtos/{id}**

    Retorna um objeto de produto no seguinte formato:

    ```json
        {
            "id": 1,
            "name": "Produto 1",
            "category": "Category 1",
            "createdAt": "2022-03-01T10:00:00Z",
            "updatedAt": "2022-03-01T10:00:00Z"
        }
    ```

* **PUT /produtos/{id}**

    Retorna um objeto de produto atualizado no seguinte formato:

    ```json
        {
            "id": 2,
            "name": "Produto Upd",
            "category": "Category 2",
            "createdAt": "2022-03-01T10:00:00Z",
            "updatedAt": "2022-03-01T10:00:00Z"
        }
    ```
    
* **POST /produtos**

    Retorna um objeto de produto criado no seguinte formato:

    ```json
        {
            "id": 3,
            "name": "Produto 3",
            "category": "Category 3",
            "createdAt": "2022-03-01T10:00:00Z",
            "updatedAt": "2022-03-01T10:00:00Z"
        }
    ```

* **DELETE /produtos/{id}**

    Retorna um status de sucesso (204 - No Content) se o produto foi excluído com sucesso.
    
## Categorias
### Endpoints

* **GET /categorias**

    Retorna uma lista de todas as categorias cadastradas no sistema.


* **GET /categorias/{id}**

    Retorna uma categoria específica pelo ID.

* **POST /categorias**

    Cria uma nova categoria com as informções fornecidas.

* **PUT /categorias/{id}**

    Atualiza uma categoria específica pelo ID.

* **DELETE /categorias/{id}**

    Exclui uma categoria específica pelo ID.

### Retornos

* **GET /categorias**

    Retorna uma lista de objetos de categoria no seguinte formato:

    ```json
        [
            {
                "id": 1,
                "name": "Category 1",
                "createdAt": "2022-03-01T10:00:00Z",
                "updatedAt": "2022-03-01T10:00:00Z"
            },
            {
                "id": 2,
                "name": "Category 2",
                "createdAt": "2022-03-01T10:00:00Z",
                "updatedAt": "2022-03-01T10:00:00Z"
            }
        ]
    ```

* **GET /categorias/{id}**

    Retorna um objeto de categoria no seguinte formato:

    ```json
        {
            "id": 1,
            "name": "Category 1",
            "createdAt": "2022-03-01T10:00:00Z",
            "updatedAt": "2022-03-01T10:00:00Z"
        }
    ```

* **PUT /categorias/{id}**

    Retorna um objeto de categoria atualizada no seguinte formato:

    ```json
        {
            "id": 2,
            "name": "Category Upd",
            "category": "Category 2",
            "createdAt": "2022-03-01T10:00:00Z",
            "updatedAt": "2022-03-01T10:00:00Z"
        }
    ```
    
* **POST /categorias**

    Retorna um objeto de categoria criada no seguinte formato:

    ```json
        {
            "id": 3,
            "category": "Category 3",
            "createdAt": "2022-03-01T10:00:00Z",
            "updatedAt": "2022-03-01T10:00:00Z"
        }
    ```

* **DELETE /categorias/{id}**

    Retorna um status de sucesso (204 - No Content) se a categoria foi excluída com sucesso.

## Clonando e Testando a Aplicação

Você pode clonar e testar a API de Usuários na sua própria máquina seguindo estes passos:

1. Abra o terminal na sua máquina e navegue até o diretório onde deseja armazenar a aplicação.

2. Execute o seguinte comando para clonar o repositório da aplicação:

    ```bash
    git clone https://github.com/seu-usuario/api-usuarios.git
    ```

3. Navegue até o diretório raiz da aplicação:

    ```bash
    cd api-usuarios
    ```
4. Execute o seguinte comando para instalar as dependências da aplicação:

    ```bash
    dotnet restore
    ```

5. Execute o seguinte comando para compilar a aplicação:

    ```bash
    dotnet build
    ```

6. Execute o seguinte comando para rodar a aplicação:

    ```bash
    dotnet run
    ```

A aplicação deverá estar sendo executada na porta 7203.

Abra o navegador e acesse a URL http://localhost:7203/produtos para testar o endpoint GET /produtos e verificar se a aplicação está funcionando corretamente.
