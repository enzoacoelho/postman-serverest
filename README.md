# 🚀 Automação de Testes de API - ServeRest (Postman)

Este repositório contém a suíte de testes automatizados de API para o endpoint `/usuarios` da aplicação **ServeRest**, desenvolvida com **Postman**.

## 📌 Funcionalidades Testadas
- **Cadastrar usuário:** Validação de status 201 e captura dinâmica de `_id` e `email`.
- **Cenários Negativos:** Tentativa de cadastro com e-mail duplicado, consulta/deleção de ID inexistente.
- **Listar usuários:** Validação da estrutura de resposta.
- **Buscar/Atualizar/Deletar usuário:** Encademamento de requisições utilizando os IDs gerados dinamicamente nos testes.

## 🛠️ Tecnologias Utilizadas
- **Postman** (Test Scripts com Chai.js)
- **ServeRest API**
- **Newman** (Execução via CLI)

## 🚀 Como Executar
1. Importe o arquivo `ServeRest.postman_collection.json` no seu Postman.
2. Defina a variável `baseUrl` no Environment ou na Collection como `https://serverest.dev/`.
3. Execute a collection usando o **Collection Runner** do Postman ou via terminal com Newman:

```bash
newman run ServeRest.postman_collection.json --env-var "baseUrl=[https://serverest.dev/](https://serverest.dev/)" 
