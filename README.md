# Docker Setup for PostgreSQL and pgAdmin

Este repositório fornece uma configuração básica do Docker Compose para executar PostgreSQL e pgAdmin.

## Requisitos

Antes de começar, certifique-se de ter os seguintes requisitos instalados em sua máquina:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Instruções

### Passo 1: Clonar o repositório

```sh
git clone o repositório
cd seu-repositorio

```

### Passo 2: Criar o arquivo .env

Crie um arquivo .env na raiz do projeto. Você pode usar o arquivo .env.example como referência. Execute o seguinte comando para criar o arquivo .env:

```sh
cp .env.example .env

```
### Passo 3: Configurar variáveis de ambiente

Abra o arquivo .env em um editor de texto e configure as variáveis de ambiente conforme necessário. Exemplo de um arquivo .env:

```sh
POSTGRES_USER=root
POSTGRES_PASSWORD=senha123
POSTGRES_DB=postgres
PGADMIN_DEFAULT_EMAIL=pgsql@mail.com
PGADMIN_DEFAULT_PASSWORD=senha123

HOST_PORT_PG=15432
HOST_PORT_PGA=8082

```

#### Passo 4: Executar o Docker Compose

Execute o seguinte comando para iniciar os contêineres:
```sh
docker-compose up -d
```

#### Passo 5: Acessando o PG Admin

configure o host do servidor como db e adicione as credenciais usadas no seu arquivo .env