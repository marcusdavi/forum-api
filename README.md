# Fórum-api
Aplicação Desenvolvida nos cursos de Spring Boot (Parte 1 e 2) do Alura. 

A API realiza um CRUD de tópicos de um fórum e roda numa base em memória (h2) populada na execução da aplicação.

### 1. Swagger (API Documentation)
* http://localhost:8080/swagger-ui.html

### 2. Endoint de autenticação
* **POST** http://localhost:8080/auth - Autenticação do usuário por login e senha dele no banco de dados. A requisição deverá ser da seguinte forma:
```
{
  "email": "aluno@email.com",
  "senha": "admin"
}
```
O resultado será um token Bearer a ser usado nos endpoints de negócio:
```
{
  "token": "<token>",
  "tipo": "Bearer"
}
```


### 3. Endoints para o Recurso 'Tópico'
* **GET** http://localhost:8080/topicos - Lista todos os tópicos do fórum;
* **GET** http://localhost:8080/topicos/{id} - Consulta um tópico com o id passado na url;
* **DELETE** http://localhost:8080/topicos/{id} - Deleta o tópico com o id passado na url;
* **POST** http://localhost:8080/topicos - Cadastra um tópico;
* **PUT** http://localhost:8080/topicos/{id} - Altera o tópico com o id passado na url.

Observação 01: Passar na requisição o token gerado no endpoint de autenticação: Bearer <token>

Observação 02: No POST e PUT também devem ser passados os dados de cadastro/alteração do tópico:
```
{
  "mensagem": "string",
  "nomeCurso": "string",
  "titulo": "string"
}
```

### 4. Como rodar a aplicação
1. Clonar o repositório
2. Importar o projeto no Eclipse/STS
3. Iniciar como SpringBoot Application






