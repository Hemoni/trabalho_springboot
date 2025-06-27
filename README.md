# 🛡️ AuthServer JWT + CRUD de Produtos

Este projeto é uma aplicação construída com **Spring Boot**, que combina autenticação via **JWT (JSON Web Token)** com um sistema de **CRUD completo de Produtos**.

---

## ⚙️ Stack Tecnológica

- Java 17
- Spring Boot 3.x
- Spring Security
- JWT (Autenticação e Autorização)
- Spring Data JPA
- Banco de Dados H2 (ou configurável para outros)
- Lombok (facilita o boilerplate)
- OpenAPI/Swagger (documentação)

---

## ✨ Recursos Disponíveis

### 🔑 Autenticação

- Criação de novos usuários
- Login com geração de token JWT
- Segurança dos endpoints com autenticação via token
- Proteção de rotas utilizando `@SecurityRequirement`
- Tokens enviados no header:
### 📦 CRUD de Produtos

- **GET** `/api/produtos` → Lista todos os produtos
- **GET** `/api/produtos/{id}` → Consulta produto pelo ID
- **POST** `/api/produtos` → Cria novo produto
- **PUT** `/api/produtos/{id}` → Atualiza produto existente
- **DELETE** `/api/produtos/{id}` → Remove produto do sistema

---

## ▶️ Como Executar

### Pré-requisitos

- Java 17 instalado
- Maven ou IDE (IntelliJ, Eclipse, VS Code) com suporte a Maven

### Passos

1. Clone o repositório:
 git clone https://github.com/seu-usuario/seu-repositorio.git
 cd authserver

2. Execute o projeto via Maven:
 ./mvnw spring-boot:run

3. Acesse a aplicação:
 http://localhost:8080

### 🗂️ Estrutura do Projeto

```plaintext
src
└── main
    ├── java/com/example/authserver
    │   ├── controller      # Controllers REST
    │   ├── model           # Entidades JPA (User, Produto)
    │   ├── repository      # Repositórios JPA
    │   ├── service         # Regras de negócio
    │   └── security        # Configuração JWT e autenticação
    └── resources
        ├── application.properties
        ├── schema.sql      # (opcional) Script para criar tabelas
        └── data.sql        # (opcional) Dados iniciais


### Exemplo de schema.sql

CREATE TABLE produto (
  id BIGINT PRIMARY KEY AUTO_INCREMENT,
  nome VARCHAR(255) NOT NULL,
  preco DECIMAL(10,2) NOT NULL
);

