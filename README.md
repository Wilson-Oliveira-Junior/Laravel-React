# Projeto Laravel e React com Docker

- Este projeto é uma aplicação full-stack que utiliza Laravel 11 como backend e React como frontend, todos rodando em contêineres Docker com um banco de dados MySQL.

## Requisitos

- Antes de começar, você precisará ter o seguinte instalado em sua máquina:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/)

## Estrutura do Projeto

/meu-projeto |-- /backend # Código fonte do Laravel |-- /frontend # Código fonte do React |-- docker-compose.yml

bash
Copiar código

## Instalação

1. **Clone o repositório**

   ```bash
   git clone https://seu-repositorio.git meu-projeto
   cd meu-projeto
Configure as variáveis de ambiente

- No diretório backend, copie o arquivo .env.example para .env e ajuste as configurações conforme necessário. Certifique-se de que as configurações do banco de dados correspondam ao serviço MySQL no docker-compose.yml.

bash
Copiar código
cd backend
cp .env.example .env
Inicie os contêineres

- Na raiz do projeto, execute o comando abaixo para iniciar os contêineres:

bash
Copiar código
docker-compose up -d
Isso iniciará os contêineres para o backend, frontend e banco de dados.

## Instale as dependências do Laravel

- Acesse o contêiner do Laravel e instale as dependências:

bash
Copiar código
docker-compose exec backend bash
composer install
php artisan key:generate
php artisan migrate
exit
## Instale as dependências do React

- Acesse o contêiner do React e instale as dependências:

bash
Copiar código
docker-compose exec frontend bash
npm install
exit
Executando a Aplicação
Após concluir as etapas de instalação, você pode acessar a aplicação:

Backend (Laravel): http://localhost:8000
Frontend (React): http://localhost:3000
Parar os Contêineres
Para parar os contêineres em execução, execute o seguinte comando:

bash
Copiar código
docker-compose down
Contribuição
Se você deseja contribuir para este projeto, sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença
Este projeto está licenciado sob a Licença MIT.
