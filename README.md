# Marketplace

## Sobre o projeto

O **Marketplace** é uma aplicação desenvolvida com o objetivo de conectar compradores e vendedores em uma plataforma digital.

A proposta é construir uma mini marketplace onde vendedores possam disponibilizar seus produtos para comercialização e compradores possam explorar as ofertas, consultar informações e realizar compras.

O projeto será desenvolvido utilizando Java e Spring Boot, seguindo boas práticas de desenvolvimento backend, organização em camadas e princípios de arquitetura de software.

## Tecnologias utilizadas

- **Java 21** – Linguagem de programação.
- **Spring Boot** – Framework para desenvolvimento da aplicação backend.
- **Gradle** – Gerenciamento de dependências e build.
- **PostgreSQL** – Banco de dados relacional.
- **Docker** – Containerização do banco de dados.

## Funcionalidades previstas

### Compradores
- Cadastro de compradores.
- Autenticação e gerenciamento de acesso.
- Consulta de produtos disponíveis.
- Pesquisa e filtros de produtos.
- Realização de pedidos.
- Acompanhamento dos pedidos.

### Vendedores
- Cadastro de vendedores.
- Gerenciamento de produtos.
- Cadastro e atualização de produtos.
- Controle de estoque.
- Gerenciamento de pedidos recebidos.

### Plataforma
- Integração entre compradores e vendedores.
- Gerenciamento de usuários.
- Catálogo de produtos.
- Gerenciamento de pedidos e seus respectivos status.

## Arquitetura

A aplicação será desenvolvida seguindo uma arquitetura em camadas, buscando manter a separação de responsabilidades e facilitar a manutenção e evolução do sistema.

Estrutura conceitual:

- **Controller:** responsável pela exposição dos endpoints REST.
- **Service:** responsável pelas regras de negócio.
- **Repository:** responsável pelo acesso e persistência dos dados.
- **Entity:** representação das entidades do domínio.
- **DTO:** objetos utilizados para transferência de dados entre as camadas.

## Pré-requisitos

Antes de executar o projeto, é necessário ter instalado:

- Java 21 ou superior.
- Docker e Docker Compose.
- Gradle (opcional, caso seja utilizado o Gradle Wrapper).

## Banco de dados

O projeto utiliza PostgreSQL como banco de dados relacional.

A configuração de conexão pode ser definida no arquivo `application.yml`:

```yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/marketplace
    username: developer
    password: 123456

  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
```

## Executando o projeto

Clone o repositório:

```bash
git clone https://github.com/amaurimotabrandao/Marketplace.git
```

Acesse a pasta do projeto:

```bash
cd marketplace
```

Inicie o banco de dados utilizando Docker Compose:

```bash
docker compose up -d
```

Execute a aplicação utilizando o Gradle Wrapper:

```bash
./gradlew bootRun
```

No Windows:

```bash
gradlew.bat bootRun
```

## Objetivo do projeto

Além de implementar uma mini marketplace funcional, o projeto tem como objetivo aplicar conceitos e boas práticas de desenvolvimento backend com Java, incluindo:

- Desenvolvimento de APIs REST.
- Programação orientada a objetos.
- Spring Data JPA e Hibernate.
- Modelagem de banco de dados relacional.
- Validação e tratamento de exceções.
- Testes automatizados.
- Boas práticas de código e princípios SOLID.
- Containerização com Docker.

---

**Status:** Em desenvolvimento.