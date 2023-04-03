# Documenta��o do ProjApiControleEstoque

Esta API � uma aplica��o desenvolvida com o framework .NET Core 6 e segue os conceitos de Domain Driven Design (DDD), com o objetivo de permitir a gest�o de estoque de produtos cadastrados no sistema. O DDD � uma abordagem de desenvolvimento de software que busca modelar o dom�nio do neg�cio de forma clara e expressiva, facilitando a evolu��o e manuten��o da aplica��o. Atrav�s das API's de Produtos e Categorias, � poss�vel realizar opera��es como cadastro, atualiza��o, exclus�o e consulta de usu�rios (C.R.U.D.), por meio de endpoints HTTP bem definidos e com respostas padronizadas.

## Documenta��o em Desenvolvimento
## Produtos
### Endpoints

* **GET /produtos**

    Retorna uma lista de todos os produtos cadastrados no sistema.


* **GET /produtos/{id}**

    Retorna um produto espec�fico pelo ID.

* **POST /produtos**

    Cria um novo produto com as informa��es fornecidas.

* **PUT /produtos/{id}**

    Atualiza um produto espec�fico pelo ID.

* **DELETE /produtos/{id}**

    Exclui um produto espec�fico pelo ID.

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

    Retorna um status de sucesso (204 - No Content) se o produto foi exclu�do com sucesso.
    
## Categorias
### Endpoints

* **GET /categorias**

    Retorna uma lista de todas as categorias cadastradas no sistema.


* **GET /categorias/{id}**

    Retorna uma categoria espec�fica pelo ID.

* **POST /categorias**

    Cria uma nova categoria com as inform��es fornecidas.

* **PUT /categorias/{id}**

    Atualiza uma categoria espec�fica pelo ID.

* **DELETE /categorias/{id}**

    Exclui uma categoria espec�fica pelo ID.

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

    Retorna um status de sucesso (204 - No Content) se a categoria foi exclu�da com sucesso.

## Clonando e Testando a Aplica��o

Voc� pode clonar e testar a API de Usu�rios na sua pr�pria m�quina seguindo estes passos:

1. Abra o terminal na sua m�quina e navegue at� o diret�rio onde deseja armazenar a aplica��o.

2. Execute o seguinte comando para clonar o reposit�rio da aplica��o:

    ```bash
    git clone https://github.com/seu-usuario/api-usuarios.git
    ```

3. Navegue at� o diret�rio raiz da aplica��o:

    ```bash
    cd api-usuarios
    ```
4. Execute o seguinte comando para instalar as depend�ncias da aplica��o:

    ```bash
    dotnet restore
    ```

5. Execute o seguinte comando para compilar a aplica��o:

    ```bash
    dotnet build
    ```

6. Execute o seguinte comando para rodar a aplica��o:

    ```bash
    dotnet run
    ```

A aplica��o dever� estar sendo executada na porta 7203.

Abra o navegador e acesse a URL http://localhost:7203/produtos para testar o endpoint GET /produtos e verificar se a aplica��o est� funcionando corretamente.
