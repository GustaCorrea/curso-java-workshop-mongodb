# Workshop Spring Boot + MongoDB (Camada de Domínio e Serviços)

[![Java Version](https://img.shields.io/badge/Java-17%20%2F%2021-orange.svg)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen.svg)](https://spring.io/projects/spring-boot)
[![MongoDB](https://img.shields.io/badge/MongoDB-NoSQL-green.svg)](https://www.mongodb.com/)

Este projeto foi desenvolvido durante o workshop prático do **Dr. Nelio Alves**, com o objetivo de construir uma API REST completa utilizando **Java**, **Spring Boot** e a base NoSQL **MongoDB**. 

A aplicação implementa o domínio de uma microrrede social, onde utilizadores podem publicar posts, interagir através de comentários e realizar buscas personalizadas.

---

## 🎯 Objetivos Principais

- Compreender e aplicar a arquitetura em camadas (Resource, Service, Repository).
- Implementar operações de CRUD completas (Create, Read, Update, Delete).
- Trabalhar com uma base de dados NoSQL (MongoDB) e compreender a diferença de modelação face ao modelo relacional.
- Tratar exceções de forma centralizada e limpa na camada de endpoints.
- Utilizar o padrão **DTO (Data Transfer Object)** para otimizar o tráfego de dados.
- Implementar consultas complexas utilizando queries personalizadas com `@Query` e métodos do Spring Data.

---

## 🏗️ Arquitetura do Projeto

O projeto segue os padrões de design de software recomendados para o ecossistema Spring:

```text
 📦 src/main/java/com/projeto
 ├── 🏢 domain          # Entidades principais (User, Post, CommentDTO)
 ├── 🗃️ repository      # Interfaces de acesso aos dados (Spring Data MongoDB)
 ├── ⚙️ services        # Camada de lógica de negócio e regras da aplicação
 ├── 🌐 resources       # Endpoints da API REST (Controllers)
 ├── 🔄 dto             # Objetos de Transferência de Dados
 └── ⚠️ exceptions      # Tratamento personalizado de erros (ResourceExceptionHandler)
