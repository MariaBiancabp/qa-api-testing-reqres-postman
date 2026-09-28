# QA API Testing - ReqRes com Postman

Projeto prático de testes de API desenvolvido no **Postman** utilizando a API pública **ReqRes**.

O objetivo é demonstrar conhecimentos básicos de testes de API, validação de respostas HTTP, criação de cenários positivos e negativos e automação de verificações com scripts no Postman.

## Tecnologias utilizadas

- Postman
- JavaScript para testes pós-resposta
- ReqRes API
- GitHub

## Cenários testados

| Método | Cenário | Resultado esperado |
|---|---|---|
| GET | Listar usuários | Status 200 e lista de usuários retornada |
| GET | Buscar usuário por ID | Status 200 e dados do usuário retornados |
| GET | Buscar usuário inexistente | Status 404 e resposta vazia |
| POST | Criar usuário | Status 201 e dados de criação retornados |
| PUT | Atualizar usuário | Status 200 e dados atualizados retornados |
| DELETE | Excluir usuário | Status 204 e resposta sem conteúdo |

## Validações automatizadas

Os requests possuem testes em **Scripts > After response** para validar, entre outros pontos:

- status code da resposta;
- formato JSON quando aplicável;
- conteúdo e estrutura dos dados retornados;
- valores esperados em campos específicos;
- geração de ID em criação de usuário;
- geração de datas de criação e atualização;
- ausência de conteúdo no DELETE.

## Cobertura dos testes

- GET - Listar usuários: **4 testes**
- GET - Buscar usuário por ID: **5 testes**
- GET - Buscar usuário inexistente: **3 testes**
- POST - Criar usuário: **6 testes**
- PUT - Atualizar usuário: **5 testes**
- DELETE - Excluir usuário: **2 testes**

**Total: 25 validações automatizadas.**

## Como executar

1. Importe o arquivo `API Testing - ReqRes.postman_collection.json` no Postman.
2. Configure a variável `reqres_api_key` com uma chave válida da ReqRes.
3. Execute os requests individualmente ou utilize o Collection Runner.
4. Consulte a aba **Test Results** para visualizar os resultados das validações.

## Segurança

A chave de API não foi incluída no repositório.

A collection utiliza a variável:

```text
{{reqres_api_key}}
```

Dessa forma, cada pessoa pode configurar sua própria chave localmente sem publicar credenciais no GitHub.

## Evidências

As evidências das execuções serão armazenadas no repositório com capturas do Postman mostrando os endpoints, status HTTP e testes executados com sucesso.

## Objetivo do projeto

Este projeto faz parte do meu portfólio de estudos em **Quality Assurance**, com foco no desenvolvimento de habilidades práticas em testes de API, análise de respostas, cenários positivos e negativos e automação de validações no Postman.
