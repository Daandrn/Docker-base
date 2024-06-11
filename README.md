Configuração básica docker com:
- php 8.3 fpm
- nginx 1.25.3
- postgres 16.1

Para iniciar os containers insira o comando:
docker-compose up -d

Para acessar o container/bash da aplicacao php:
docker-compose exec app bash

Para acessar o container do postgres:
docker-compose exec postgres psql -U postgres

Para acessar o container/bash do nginx:
docker-compose exec nginx bash

Para reiniciar os containers insira o comando:
docker-compose restart

Para encerrar os containers insira o comando:
docker-compose down
