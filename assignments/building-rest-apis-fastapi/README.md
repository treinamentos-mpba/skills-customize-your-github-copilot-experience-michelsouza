# 📘 Atividade: Building REST APIs com FastAPI

## 🎯 Objetivo

Construa uma API REST para gerenciar tarefas usando FastAPI. Pratique criação de rotas, validação de dados com modelos, operações CRUD e respostas HTTP apropriadas.

## 📝 Tarefas

### 🛠️ Criar a aplicação e as rotas de listagem e criação

#### Descrição
Configure uma aplicação FastAPI para gerenciar tarefas. Cada tarefa deve ter um identificador, um título e um indicador de conclusão. Nesta primeira etapa, implemente as rotas para listar e criar tarefas.

#### Requisitos
O programa concluído deve:

- Criar uma aplicação FastAPI que possa ser iniciada com Uvicorn.
- Definir um modelo de dados para as tarefas, com `id` inteiro, `title` textual e `completed` booleano, que começa como `false`.
- Implementar `GET /tasks` para retornar as tarefas armazenadas.
- Implementar `POST /tasks` para receber uma tarefa em JSON, atribuir um identificador e adicioná-la à coleção.
- Retornar o código HTTP `201 Created` ao criar uma tarefa.
- Manter os dados em memória; não é necessário configurar um banco de dados.

### 🛠️ Implementar as operações restantes e tratar erros

#### Descrição
Complete a API permitindo consultar, atualizar e excluir uma tarefa específica. Trate identificadores inexistentes e valide os dados recebidos.

#### Requisitos
O programa concluído deve:

- Implementar `GET /tasks/{task_id}` para retornar uma tarefa específica.
- Implementar `PUT /tasks/{task_id}` para atualizar o título e o estado de conclusão.
- Implementar `DELETE /tasks/{task_id}` para excluir uma tarefa.
- Retornar `404 Not Found` quando uma operação solicitar um identificador que não existe.
- Rejeitar títulos vazios usando validação do modelo de entrada.
- Retornar `204 No Content` ao excluir uma tarefa com sucesso.
- Permitir testar as rotas pela documentação interativa disponível em `/docs`.
