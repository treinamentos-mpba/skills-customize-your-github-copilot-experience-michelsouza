# 📘 Atividade: Persistência de Dados com FastAPI e SQLite

## 🎯 Objetivo

Adapte uma API CRUD de tarefas feita com FastAPI para armazenar os dados em SQLite em vez de mantê-los apenas em memória. Pratique criação de tabelas, consultas SQL parametrizadas e integração entre persistência e rotas HTTP.

## 📝 Tarefas

### 🛠️ Criar a tabela e as operações de persistência

#### Descrição
Configure o banco SQLite da aplicação e implemente as operações necessárias para criar e consultar tarefas. Inicialize a estrutura do banco quando a aplicação iniciar.

#### Requisitos
O programa concluído deve:

- Usar o módulo `sqlite3` da biblioteca padrão do Python.
- Criar um arquivo de banco de dados chamado `tasks.db` e uma tabela `tasks` com `id`, `title` e `completed`.
- Definir `id` como chave primária gerada pelo banco, exigir um título e iniciar `completed` como falso.
- Implementar operações para inserir tarefas e consultar uma tarefa pelo identificador ou listar todas.
- Usar parâmetros nas consultas SQL em vez de concatenar valores recebidos do usuário.
- Fechar as conexões com o banco após cada operação e confirmar as alterações realizadas.

### 🛠️ Conectar as rotas CRUD ao SQLite

#### Descrição
Substitua o armazenamento em memória da API por operações no banco de dados. Preserve o comportamento das rotas e valide a persistência reiniciando o servidor.

#### Requisitos
O programa concluído deve:

- Implementar `GET /tasks` para listar as tarefas armazenadas.
- Implementar `POST /tasks` para criar uma tarefa e retornar `201 Created`.
- Implementar `GET /tasks/{task_id}` para consultar uma tarefa específica.
- Implementar `PUT /tasks/{task_id}` para atualizar o título e o estado de conclusão.
- Implementar `DELETE /tasks/{task_id}` para excluir uma tarefa e retornar `204 No Content`.
- Retornar `404 Not Found` quando uma operação solicitar uma tarefa inexistente.
- Preservar os dados após encerrar e iniciar o servidor novamente.
