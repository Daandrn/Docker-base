1. Instalar o docker desktop, para o windows
2. Instalar o wsl 2 versao ubuntu (Utilizar sempre o wsl para docker e laravel)
3. criar pasta que será usada com "mkdir nome-pasta", acessar pasta com "cd nome-pasta"
4. usar o comando 'cp .env.example .env' bash no wsl para criar copia do arquivo .env
5. usar o comando 'docker-compose up -d' para subir as imagens configuradas no docker file (verificar se o container já nao esta ativo com 'docker ps' fora do bash do app)
6. usar o comando 'docker-compose exec app bash' para abrir CMD no container 'app', que pode ser visualizado no arquivo 'docker-compose.yml'. 
    6. 1. dentro do bash do container do app:
    6. 2. usar o comando 'composer install/update' para instalar as dependencias do laravel
    6. 3. usar o comando 'php artisan key:generate' para gerar a chave de criptografia da aplicação na base 64 (pode conferir no arquivo .env)

7. no arquivo 'docker-compose.yml' contém todas as configurações das imagens como portas, senhas, nome de base de dados, senha e etc
8. no primeiro commit precisa do e-mail e nome como abaixo:
    git config --global user.email "dandrn7@gmail.com"
    git config --global user.name "Danillo Rodrigues"
9. Publicar a branch com o comando: 'git remote add origin https://github.com/Daandrn/teste.git' | link de exemplo
10. renomeia a branch: git branch -M main
11. alterar o timezone no config/app.php para 'America/Sao_Paulo'

\\\\\\\\\\ Comandos Postgres \\\\\\\\\\
- docker-compose exec postgres psql -U postgres -d postgres \\ abre o terminal do psql com o usuário postgres
- \l \\ lista as bases de dados
- \c <nome_base> \\ entra na base
- \dt \\ lista todas tabelas
- \q \\ para sair do psql

\\\\\\\\\\ Comandos Linux \\\\\\\\\\
- mkdir nome-pasta \\ cria nova pasta
- cp <nome-arquivo> <novo-nome-copia> \\ cria copia do arquivo com nome especificado
- sudo rm -r <nome-pasta> \\ exclui pasta de forma recursiva
- sudo nano <nome-arquivo> \\ abre o editor de texto direto no cmd (também serve para criar arquivo)
- code . \\ abre o diretório no vscode

\\\\\\\\\\ comandos Docker \\\\\\\\\\
- docker ps \\ lista containers ativos
- docker-compose up -d \\ Inicia os containers
- docker-compose restart \\ Reinicia todos os containers
- docker-compose down \\ para todos os containers
- docker image build --no-cache -t app . \\ roda os arquivos docker novamente sem cache (o . define que será no diretório atual)
- docker-compose exec app bash \\ abre a aplicação no bash (útil para composer, artisan e php)

\\\\\\\\\\ Comandos Composer \\\\\\\\\\
- composer update \\ Atualiza dependencias

\\\\\\\\\\ Comandos Artisan \\\\\\\\\\
- php artisan install \\ Instala migrates
- php artisan migrate \\ Rodar as migrates