# Projeto RH Queens 

**Link do Repositório**: [https://github.com/maytearaujo/rh-queens.git](https://github.com/maytearaujo/rh-queens.git)  
**Projeto**: Cadastro RH

---

### Integrantes: 🤝
- **Abiqueila**: [GitHub](https://github.com/Abilafora/)
- **Ana Beatriz**: [GitHub](https://github.com/dsilvasantosgit)
- **Evelyn Pereira**: [GitHub](https://github.com/EvelynSantos6) 
- **Hellen Gleice**: [GitHub](https://github.com/hellengleice) 
- **Isabela Santos**: [GitHub](https://github.com/Isabela-prog)
- **Maytê Araújo**: [GitHub](https://github.com/maytearaujo)
- **Thainara Cruz**: [GitHub](https://github.com/ThainaraCruz)

---

### Objetivo: 🎯
Criar um projeto **Spring Boot** para um sistema de **cadastro de funcionários**.

---

### Packages Utilizados: 🛠️
- **Model**: Representa os dados (Postagem).
- **Postagem Controller**: Controlador para manipulação das requisições.
- **Repository**: Camada responsável pela comunicação com o banco de dados.

---

### Etapas do Projeto: 🔧

#### 1. Criação do Projeto Spring:
- Nome do projeto: **Rh Queens**.

#### 2. Configuração da Conexão com o Banco de Dados:
- Conexão configurada corretamente para persistir os dados.

#### 3. Criação do Package **model**:
- Definição dos atributos para a classe **Funcionario**.
- Implementação de **getters** e **setters** para acessar e modificar os dados.

#### 4. Criação do Package **repository**:
- Implementação do repositório usando **JPA** (Java Persistence API).
- Usamos o **extends JpaRepository** para facilitar a comunicação com o banco de dados.

#### 5. **DER Tabela Funcionários** 📊

#### 6. Criação dos Endpoints (API RESTful) 🌐:
- **GET** (Buscar todos os funcionários):
  - Utilizamos **JPA** para buscar todos os funcionários.
  - Configuração do **GET mapping** para a rota `/funcionarios`.
  - Testado utilizando **Insomnia** (requisição GET).
  
- **GET** (Buscar por ID):
  - Criação do **GET mapping** para buscar um funcionário por **ID**.
  - Testado utilizando **Insomnia** (requisição GET).

- **GET** (Buscar por nome):
  - Criação do **GET mapping** para buscar um funcionário pelo **nome**.
  - Rota configurada: `/funcionarios/nome/{nome}`.
  - Testado utilizando **Insomnia** (requisição GET).

- **POST** (Cadastrar funcionário):
  - Criação do **POST mapping** para cadastrar um novo funcionário.
  - Testado utilizando **Insomnia** (requisição POST).

- **PUT** (Atualizar funcionário):
  - Criação do **PUT mapping** para atualizar os dados de um funcionário existente.
  - Testado utilizando **Insomnia** (requisição PUT).

- **DELETE** (Deletar funcionário):
  - Criação do **DELETE mapping** para excluir um funcionário.
  - Testado utilizando **Insomnia** (requisição DELETE).

---

### Tecnologias Utilizadas: 🖥️
- **Spring Framework**: Framework principal para desenvolvimento da aplicação.
- **Spring Boot**: Facilita a criação e configuração do projeto Spring. Configuração automática de servidores embutidos (como Tomcat e Jetty) e simplificação da criação de APIs RESTful.
- **JPA (Java Persistence API)**: Usado para mapear objetos Java para tabelas de bancos de dados relacionais.
- **Spring Web**: Facilita a criação de APIs RESTful. Usamos **@RestController** e **@RequestMapping** para definir as rotas e métodos de manipulação de requisições.
- **Insomnia**: Ferramenta de cliente HTTP para testar e depurar APIs RESTful. Essencial para realizar testes das APIs criadas com Spring Boot, validando as requisições **GET**, **POST**, **PUT**, e **DELETE**.
