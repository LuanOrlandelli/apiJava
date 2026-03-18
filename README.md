# 🧠 SkillBridge API - GS 2025

API RESTful desenvolvida para promover **Upskilling e Reskilling** de profissionais, com foco em trilhas de aprendizagem e usuários, alinhada aos pilares da transformação digital e educação continuada.

---

## ✅ README, Execução e Boas Práticas

Este documento contém as instruções necessárias para compreender, executar e testar a API `SkillBridge`, além de evidenciar boas práticas utilizadas no projeto.

---

## 📌 Versões Utilizadas

- **Java:** 21  
- **Framework:** Spring Boot 3.2.0  
- **Gerenciador de dependências:** Maven  
- **Banco de dados:** H2 (memória)

---

## 🚀 Como Subir o Projeto

### 1. Pré-requisitos

- JDK 21 instalado e configurado
- Maven instalado (`mvn -v` deve funcionar no terminal)
- IDE recomendada: IntelliJ IDEA

### 2. Passos

```bash
# 1. Clonar ou extrair o projeto
# 2. Entrar na pasta do projeto
cd skillbridge-api

# 3. Executar o projeto
mvn spring-boot:run
```

### 3. Acessos

- API: [http://localhost:8080](http://localhost:8080)
- Console do banco H2: [http://localhost:8080/h2-console](http://localhost:8080/h2-console)  
  - JDBC URL: `jdbc:h2:mem:skillbridge`
  - Usuário: `sa` / Senha: *(em branco)*

---

## 🧪 Como Testar a API

Recomenda-se o uso do **Postman**.

### Exemplo - Criar Usuário
```json
POST /api/usuarios
{
  "nome": "Carlos Lima",
  "email": "carlos@email.com",
  "areaAtuacao": "TI",
  "nivelCarreira": "Junior"
}
```

### Exemplo - Criar Trilha
```json
POST /api/trilhas
{
  "nome": "Java Backend",
  "descricao": "Spring Boot com Java",
  "nivel": "INICIANTE",
  "cargaHoraria": 30,
  "focoPrincipal": "Back-end"
}
```

---

## 🧱 Arquitetura do Projeto

- **Java 21**
- **Spring Boot 3.2+**
- Spring Web, Spring Data JPA, Lombok, Bean Validation
- **Banco de dados:** H2 (em memória)
- Estrutura em camadas (MVC + DDD):
  - `controller`, `service`, `repository`, `model`, `dto`, `exception`

---

## 📦 Entidades e Recursos

### 👤 Usuários

| Método | Endpoint            | Função                |
|--------|----------------------|------------------------|
| GET    | `/api/usuarios`     | Listar todos os usuários |
| GET    | `/api/usuarios/{id}`| Buscar usuário por ID |
| POST   | `/api/usuarios`     | Criar novo usuário     |
| PUT    | `/api/usuarios/{id}`| Atualizar usuário      |
| DELETE | `/api/usuarios/{id}`| Deletar usuário        |

---

### 🧭 Trilhas de Aprendizagem

| Método | Endpoint            | Função                  |
|--------|----------------------|--------------------------|
| GET    | `/api/trilhas`      | Listar todas as trilhas |
| GET    | `/api/trilhas/{id}` | Buscar trilha por ID    |
| POST   | `/api/trilhas`      | Criar nova trilha       |
| PUT    | `/api/trilhas/{id}` | Atualizar trilha        |
| DELETE | `/api/trilhas/{id}` | Deletar trilha          |

---

## 💾 Banco de Dados

Banco em memória H2 configurado em `application.properties`.

```
spring.datasource.url=jdbc:h2:mem:skillbridge
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=create
spring.h2.console.enabled=true
```

🔗 Acesse: [http://localhost:8080/h2-console](http://localhost:8080/h2-console)  
JDBC URL: `jdbc:h2:mem:skillbridge`  
Usuário: `sa`  
Senha: *(em branco)*

---

## ✅ Funcionalidades Atendidas

✔ CRUD completo de todos os recursos implementados  
✔ DTOs para entrada de dados  
✔ Validação com Bean Validation  
✔ Exceções personalizadas  
✔ Banco com dados de teste (`data.sql`)  
✔ H2 Console ativado  
✔ Código organizado em camadas (Controller, Service, Repository, Model, DTO)  
✔ README claro e estruturado ✅

---

## ✅ Organização e Boas Práticas

- 📦 **Estrutura em camadas (MVC + DDD)**:
  - `controller`, `service`, `repository`, `model`, `dto`, `exception`
- ✅ **DTOs** para entrada de dados
- ✅ **Validações com Bean Validation**
- ✅ **Tratamento de exceções global customizado**
- ✅ **Banco de dados de teste via H2**
- ✅ **Legibilidade e nomeação clara** de variáveis, métodos e classes
- ✅ **Uso correto de anotações** do Spring e Java

---


## 🎥 Vídeo Testando a API com o Postman (Collection disponibilizada no repostório)
- https://drive.google.com/file/d/1hK8DTMp-f2QjfNxXiyvmeVdsFIjFIavp/view?usp=sharing

---

## 👨‍💻 Autor

 ### Desenvolvido por: 
 - Luan Orlandelli Ramos - 554747

 ### Curso: 
 - Engenharia de Software 
 - 2ESPY
 - DOMAIN DRIVEN DESIGN – JAVA
 
