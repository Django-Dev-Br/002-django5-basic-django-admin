
# 002 Django 5 - Admin Setup

No [repositório anterior](https://github.com/Django-Dev-Br/001-django5-basic-project) criamos um projeto Django. 

Agora, dando sequência, vamos materializar a estrutura de tabelas do banco de dados que vem com o Django. Em seguida, vamos criar um superusuário para acessar o Django-Admin. 

Nos repositórios seguines,[03](https://github.com/Django-Dev-Br/003-django5-fixtures) e [04](https://github.com/Django-Dev-Br/004-django5-dot-env-file), vamos adicionar algumas configurações adicionais, seguindo boas práticas de mercado.

Nos repositórios [05](https://github.com/Django-Dev-Br/005-Django5-Basic-App) e [06](https://github.com/Django-Dev-Br/006-Django5-Basic-App-2) vamos adicionar um app ao Projeto. 

Esses 06 primeiros respositórios supracitados compõem um scaffold ou o core para o desenvolvimento de uma aplicação web com Python e Django. 

### O que é o Django Admin?

O Django Admin é uma interface administrativa gerada automaticamente por meio das configurações do projeto Django. Ele permite gerenciar modelos (tabelas de bancos de dados) e realizar operações CRUD (Criar, Ler, Atualizar, Deletar) de forma rápida e eficiente. O Django Admin é uma ferramenta poderosa para gerenciar o conteúdo e as funcionalidades do seu site diretamente a partir do navegador.

[confira o melhor material de toda a internet sobre o assunto:](https://books.agiliq.com/projects/django-admin-cookbook/en/latest/)

**OBS**: Confira no [repositório anterior](https://github.com/Django-Dev-Br/001-django4-basic-project) os conceitos de **Projeto Django, venv, PIP e PyPi**. 

## COMO RODAR ESSE PROJETO EM SEU COMPUTADOR:

### Requisitos

- **Python 3.12 com PIP e venv**
-  **o Django 5 requer Python 3.10 ou superior.**

- **No [repositório anterior](https://github.com/Django-Dev-Br/001-django4-basic-project) há explicações sobre PIP e venv**

  [Baixar Python 3.12](https://www.python.org/downloads/release/python-3122/)

  Confira o vídeo para saber como trabalhar com múltiplas versões do Python e com venv (ambiente virtual):
  [![Watch the video](https://img.youtube.com/vi/eetDeQrv0Rs/0.jpg)](https://youtu.be/eetDeQrv0Rs)


### 8 passos simples para executar

1. **Clone o repositório**:
    ```bash
    git clone https://github.com/Django-Dev-Br/002-django5-basic-django-admin.git
    ```

2. **Crie um ambiente virtual**:
   
    **Windows**
    ```bash
     python -m venv myvenv  
    ```
   **Linux**
    ```bash
     python3 -m venv myvenv  
    ```

3. **Ative o ambiente virtual criado**:
   
    **Windows**
    ```bash
    myvenv\Scripts\activate  
    ```

   **Linux**
    ```bash
    source myvenv/bin/activate  
    ```

4. **Instale o Django**:
    ```python
    pip install django==4.2.15
    ```
    - use, preferencialmente, a versão 5.1. Para tanto, execute o comando:

     ```bash
    pip install  "django>=5.1,<=5.2"
    ```

5. **Acesse a pasta do projeto Django**
   ```bash
    cd 002-django5-basic-django-admin
    ```
   
6. **Execute as migrações do banco de dados**:
    ```bash
    python manage.py migrate
    ```
    O comando acima criará no diretório raiz o banco de dados db.sqlite3 com o esquema de tabelas do Django

7. **Crie um superusuário para acessar o Django Admin**:
    ```bash
    python manage.py createsuperuser
    ```
    Após, siga as instruções do terminal para criar um usuário e senha. Em regra, usa-se, respectivamente, admin e root. Não é preciso informar o email em ambiente local.

   **OBS:** No [próximo repositório desta série](https://github.com/Django-Dev-Br/003-django5-fixtures), iremos ver como criar um arquivo de backup desse superusuário ora criado.

8. **Execute o servidor de desenvolvimento**:
    ```bash
    python manage.py runserver
    ```

### Acesse o Django Admin no seu navegador:

Após executar o servidor de desenvolvimento, você pode acessar o Django Admin no seguinte endereço:

[http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

Faça login com as credenciais do superusuário que você acabou de criar.


### Estrutura de Diretórios do Projeto

```
002-django4-admin-setup/
├── .gitignore           # Arquivo que especifica quais arquivos e diretórios o Git deve ignorar (não incluir no versionamento)
├── db.sqlite3           # Banco de dados SQLite criado após as migrações
├── myproject/
│   ├── __init__.py      # Marca o diretório como um pacote Python
│   ├── asgi.py          # Configurações para o servidor ASGI (usado para aplicações assíncronas)
│   ├── settings.py      # Configurações do projeto (banco de dados, apps instalados, etc.)
│   ├── urls.py          # Mapeamento de requisições HTTP e redirecionamento para os templates HTML
│   └── wsgi.py          # Configurações para o servidor WSGI (usado para servir a aplicação)
└── manage.py            # CLI do Django, um script de linha de comando para tarefas execução de comandos do Django no terminal
```

### OBS: Como Criar um Projeto Django

Se desejar criar seu próprio projeto Django, use o seguinte comando após criar e ativar a virtual env e instalar o django nela, conforme orientações acima:

```bash
django-admin startproject myproject
```

### Sobre Nosso Treinamento Prático-Profissional com projeto real para iniciantes e avançados em web DevOps Full-stack com Python, Django, Bootstrap e Linux.

[Django Developers Brasil - Aprenda programando enquanto programa aprendendo!](https://django.dev.br/)

Nosso treinamento oferece uma experiência prática de aprendizado de programação, adequada tanto para iniciantes quanto para desenvolvedores avançados. Você participará de um projeto real de desenvolvimento de software em um ambiente corporativo autêntico, onde pessoas com diferentes níveis de conhecimento irão colaborar, aprendendo umas com as outras.

**Junte-se a nós!** E desenvolva as habilidades necessárias para o mercado de trabalho, aprimorando tanto seus conhecimentos técnicos quanto suas soft skills em um ambiente colaborativo e realista.
