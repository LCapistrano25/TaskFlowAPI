# TaskFlow API - Soluções Internet

Este projeto é uma API de gerenciamento de tarefas (Task Management) desenvolvida com Django e Django REST Framework (DRF). Ele permite a criação de tarefas, categorias, prioridades e gerenciamento de usuários e grupos, utilizando autenticação via JWT.

## 🚀 Funcionalidades

- **Autenticação:** Login e geração de tokens JWT.
- **Usuários:** Gerenciamento de usuários.
- **Grupos:** Organização de usuários em grupos (equipes).
- **Tarefas:** Criação, edição e exclusão de tarefas.
- **Categorias e Prioridades:** Organização e classificação das tarefas.
- **Validação de Datas:** Garantia de que a data de término não seja anterior à data de início.

## 🛠️ Tecnologias Utilizadas

- [Python](https://www.python.org/)
- [Django](https://www.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [Simple JWT](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/)
- [SQLite](https://www.sqlite.org/) (Banco de dados padrão)

## 📋 Pré-requisitos

- Python 3.10 ou superior
- Pip (gerenciador de pacotes do Python)

## 🔧 Instalação

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/seu-usuario/API-Solucoes-Internet.git
    cd API-Solucoes-Internet
    ```

2.  **Crie e ative um ambiente virtual:**
    ```bash
    # No Windows
    python -m venv venv
    .\venv\Scripts\activate

    # No Linux/macOS
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Instale as dependências:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Execute as migrações do banco de dados:**
    ```bash
    python manage.py migrate
    ```

5.  **Crie um superusuário (opcional, para acessar o admin):**
    ```bash
    python manage.py createsuperuser
    ```

6.  **Inicie o servidor de desenvolvimento:**
    ```bash
    python manage.py runserver
    ```
    A API estará disponível em `http://127.0.0.1:8000/`.

## 📖 Documentação da API (Endpoints)

Abaixo estão alguns dos principais endpoints disponíveis:

- **Autenticação:**
  - `POST /api/token/`: Obter token JWT (login).
  - `POST /api/token/refresh/`: Atualizar token JWT.

- **Usuários:**
  - `GET/POST /api/users/`: Listar ou criar usuários.

- **Tarefas:**
  - `GET/POST /api/tasks/`: Listar ou criar tarefas.
  - `GET/PUT/DELETE /api/tasks/{id}/`: Detalhes, editar ou excluir uma tarefa.

- **Categorias:**
  - `GET/POST /api/categories/`: Gerenciar categorias de tarefas.

- **Prioridades:**
  - `GET/POST /api/priorities/`: Gerenciar níveis de prioridade.

## 📁 Estrutura do Projeto

- `taskflow/`: Configurações principais do projeto Django.
- `authentication/`: App responsável pela lógica de autenticação.
- `users/`: App de gerenciamento de usuários.
- `groups/`: App de gerenciamento de grupos/equipes.
- `tasks/`: App principal de tarefas, categorias e prioridades.
- `manage.py`: Script de gerenciamento do Django.
- `requirements.txt`: Lista de dependências do projeto.
