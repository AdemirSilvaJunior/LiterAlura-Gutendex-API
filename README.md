# LiterAlura - Gutendex API

![Java](https://img.shields.io/badge/Java-11-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.5.4-green)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13-blue)

Este projeto foi desenvolvido como parte do desafio LiterAlura da Alura, utilizando a API Gutendex para construir um catálogo de livros.

## Descrição

O LiterAlura-Gutendex-API é um projeto Java com Spring Boot que permite interações básicas com uma base de dados de livros. Utiliza a API Gutendex para buscar informações de livros e as armazena em um banco de dados PostgreSQL.

## Funcionalidades

- Busca de livros pelo título na API Gutendex e armazenamento no banco de dados
- Listagem de todos os livros registrados
- Listagem de autores e seus respectivos livros
- Listagem de autores que estavam vivos em um determinado ano
- Listagem de livros por idioma disponível no banco de dados

## Tecnologias Utilizadas

- **Java:** Linguagem de programação utilizada no projeto.
- **Spring Boot:** Framework utilizado para desenvolvimento de aplicações Java.
- **Spring Data JPA:** Facilita o acesso e a persistência de dados em bancos de dados relacionais com o Spring Framework.
- **PostgreSQL:** Sistema gerenciador de banco de dados relacional utilizado para armazenamento dos dados.
- **API Gutendex:** API gratuita que fornece dados de mais de 70 mil livros da biblioteca online Projeto Gutenberg.

## Configuração do Projeto

### Pré-requisitos

- JDK 11 ou superior instalado
- Maven para gerenciamento de dependências
- PostgreSQL instalado e configurado

### Configuração do Banco de Dados

1. Crie um banco de dados PostgreSQL chamado `literalura_db`.
2. Configure as credenciais do banco de dados no arquivo `application.properties` do projeto:

### Executando o Projeto
Clone o repositório:
bash
Copiar código
git clone https://github.com/seu_usuario/LiterAlura-Gutendex-API.git
### Navegue até o diretório do projeto:
bash
Copiar código
cd LiterAlura-Gutendex-API
### Execute o projeto com Maven:
bash
Copiar código
mvn spring-boot:run
O servidor será iniciado em http://localhost:8080.

### Endpoints
GET /livros: Retorna todos os livros armazenados no banco de dados.
GET /autores: Retorna todos os autores e seus respectivos livros.
GET /autores/{ano}: Retorna autores que estavam vivos no ano especificado.
GET /livros/idioma/{idioma}: Retorna livros filtrados pelo idioma especificado.
Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para enviar pull requests ou abrir issues para sugestões e problemas encontrados.

### Configuração do Banco de Dados

1. Crie um banco de dados PostgreSQL chamado `literalura_db`.
2. Configure as credenciais do banco de dados no arquivo `application.properties` do projeto:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/literalura_db
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.datasource.driver-class-name=org.postgresql.Driver
spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
