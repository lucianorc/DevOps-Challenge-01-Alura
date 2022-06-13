# Challenge DevOps 01 Alura

Repositório para desafio Alura DevOps

## How to run

- Em um virtual environment
```sh
$ virtualenv venv
$ pip install -r requirements.txt # Instalar dependências
$ python manager migrate # Para migrar definições de tabelas no banco de dados
$ python manager createsuperuser # Para criar um Super Usuário para controlar o sistema
$ python manager runserver 0.0.0.0:8000 # Para rodar servidor WSGI respondendo para todos os hosts na porta 8000
```

- Usando Docker
```sh
$ docker build -t aluraflix .
$ docker run -p 8000:8000 -n aluraflix aluraflix # Para rodar servidor WSGI respondendo para todos os hosts na porta 8000
$ docker exec -it aluraflix python manager migrate # Para migrar definições de tabelas no banco de dados
$ docker exec -it aluraflix python manager createsuperuser # Para criar um Super Usuário para controlar o sistema
```