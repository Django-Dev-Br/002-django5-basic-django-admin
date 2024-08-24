
# 002 Django 4 Admin Setup

## COMO RODAR ESSE PROJETO EM SEU COMPUTADOR:

### Requisitos

- **Python 3.12**  
  [Baixar Python 3.12](https://www.python.org/downloads/release/python-3122/)

  Confira o vídeo para saber como trabalhar com múltiplas versões do Python e com venv (ambiente virtual): [Trabalhando com Múltiplas Versões do Python + venv](https://youtu.be/eetDeQrv0Rs?si=rAIDmLCgdeh7ouXa)

- **Virtualenv**

  Para instalar o pacote `virtualenv` no Python, utilize os seguintes comandos:

  - **Linux**:
    ```bash
    python3 -m pip install virtualenv
    ```

  - **Windows**:
    ```bash
    python -m pip install virtualenv
    ```

### Passos para Executar

1. **Clone o repositório**:
    ```bash
    git clone https://github.com/Django-Dev-Br/002-django4-basic-django-admin.git
    cd 002-django4-basic-django-admin
    ```

2. **Crie um ambiente virtual**:
    ```bash
    python3 -m venv myvenv  # Linux
    python -m venv myvenv  # Windows
    ```

3. **Ative o ambiente virtual criado**:
    ```bash
    source myvenv/bin/activate  # Linux
    myvenv\Scripts\activate  # Windows
    ```

4. **Instale o Django**:
    ```bash
    pip install django==4.2.15
    ```

5. **Execute as migrações do banco de dados**:
    ```bash
    python manage.py migrate
    ```

6. **Crie um superusuário para acessar o Django Admin**:
    ```bash
    python manage.py createsuperuser
    ```

7. **Execute o servidor de desenvolvimento**:
    ```bash
    python manage.py runserver
    ```

### Acesse o Django Admin no seu navegador:

Após executar o servidor de desenvolvimento, você pode acessar o Django Admin no seguinte endereço:

[http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

Faça login com as credenciais do superusuário que você acabou de criar.

### O que é o Django Admin?

O Django Admin é uma interface administrativa gerada automaticamente por meio das configurações do projeto Django. Ele permite gerenciar modelos e realizar operações CRUD (Criar, Ler, Atualizar, Deletar) de forma rápida e eficiente. O Django Admin é uma ferramenta poderosa para gerenciar o conteúdo e as funcionalidades do seu site diretamente a partir do navegador.

### Estrutura de Diretórios do Projeto

```
002-django4-admin-setup/
├── myproject/
│   ├── __init__.py      # Marca o diretório como um pacote Python
│   ├── asgi.py          # Configurações para o servidor ASGI (usado para aplicações assíncronas)
│   ├── settings.py      # Configurações do projeto (banco de dados, apps instalados, etc.)
│   ├── urls.py          # Mapeamento de requisições HTTP e redirecionamento para os templates HTML
│   └── wsgi.py          # Configurações para o servidor WSGI (usado para servir a aplicação)
└── manage.py            # CLI do Django, um script de linha de comando para tarefas administrativas do Django
```

### Sobre Nosso Treinamento Prático-Profissional com projeto real para iniciantes e avançados em web DevOps Full-stack com Python, Django, Bootstrap e Linux.

[Django Developers Brasil - Aprenda programando enquanto programa aprendendo!](https://django.dev.br/)

Nosso treinamento oferece uma experiência prática de aprendizado de programação, adequada tanto para iniciantes quanto para desenvolvedores avançados. Você participará de um projeto real de desenvolvimento de software em um ambiente corporativo autêntico, onde pessoas com diferentes níveis de conhecimento irão colaborar, aprendendo umas com as outras.

**Junte-se a nós!** E desenvolva as habilidades necessárias para o mercado de trabalho, aprimorando tanto seus conhecimentos técnicos quanto suas soft skills em um ambiente colaborativo e realista.
