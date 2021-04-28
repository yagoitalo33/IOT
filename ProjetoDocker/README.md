
<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href=" https://github.com/iLudolf/IOT.git">
    <img src="https://i1.wp.com/www.docker.com/blog/wp-content/uploads/2020/02/Compose.png?resize=200%2C219&ssl=1" alt="Logo" width="100" height="100">
  </a>

  <h3 align="center">SISTEMAS DISTRIBUÍDOS</h3>
  <p align="center">  Trabalho Contêineres </p>


<!-- ABOUT THE PROJECT -->
## Especificações do trabalho
<!-- 
[![Product Name Screen Shot][product-screenshot]](https://example.com) -->

Configurar um ambiente baseado em contêineres Docker com a seguinte especificação:
* 1 contêiner com um servidor web e o sistema `PHP` disponibilizado em anexo.
* 1 contêiner com um servidor de banco de dados `MySQL` com a estrutura de dados
disponibilizada em anexo
* 1 contêiner com `PHPMyAdmin` para administração da base de dados MySQL

O servidor web deve disponibilizar o sistema PHP na porta 80 da máquina local. Esse sistema
deve ser capaz de acessar o servidor MySQL que está executando no outro contêiner. O MySQL
deve ser capaz de armazenar seus arquivos de dados de alguma forma definitiva (sendo que, ao
se desligar o contêiner, os dados não se perdem). O sistema como um todo deve ser executado
através do Docker Compose, garantindo assim que as partes que compõem o serviço serão
corretamente executadas.

Deve haver um quarto contêiner executando o portainer.io (http://portainer.io). Este contêiner
deve ser capaz de gerenciar de forma gráfica os contêineres em execução localmente.
Todo o ambiente deve estar funcional

### Docker Hub

* [MySQL](https://hub.docker.com/_/mysql)
* [phpMyAdmin](https://hub.docker.com/_/phpmyadmin)
* [Portainer](https://hub.docker.com/r/portainer/portainer)

O build da imagem `php_app` será criada na execução do docker compose.

<!-- GETTING STARTED -->
## Pré-requisitos para rodar o projeto:

* Você deve ter o Docker e o Docker Compose (versões recentes) instalados;

## Como rodar o projeto

1. Faça o download do diretório (ou faça um clone deste repositório inteiro);
   ```sh
   git clone https://github.com/iLudolf/IOT.git
   ```
2. Executar o docker-compose na raiz do projeto via terminal
   ```sh
   Docker-compose -f Docker-compose.yml up -d --build
   ```
Após todo processo de build do Docker ser concluído, você só precisa importar a tabela do banco de dados, que está localizada no diretório: 

  ```sh
  ./mysql/database/employees.sql
   ```
Todo processo de importar a tabela `employees.sql`, pode ser realizada diretamente pelo phpMyAdmin.

### URL

* [Aplicativo php](http://localhost/)
* [phpMyAdmin](http://localhost:8080/)
* [Portainer](http://localhost:9000/)


 