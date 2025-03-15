# Projeto RH Queens

Sistema de cadastro RHQueens.

**Projeto**: Cadastro RH

## Integrantes

- [Abiqueila](https://github.com/Abilafora/)
- [Ana Beatriz](https://github.com/dsilvasantosgit)
- [Evelyn Pereira](https://github.com/EvelynSantos6)
- [Hellen Gleice](https://github.com/hellengleice)
- [Isabela Santos](https://github.com/Isabela-prog)
- [Maytê Araújo](https://github.com/maytearaujo)
- [Thainara Cruz](https://github.com/ThainaraCruz)

## Objetivo

Criar um projeto Spring Boot para um sistema de cadastro de funcionários.

## Packages Utilizados

- **Model**: Representa os dados (Funcionario).
- **Postagem Controller**: Controlador para manipulação das requisições.
- **Repository**: Camada responsável pela comunicação com o banco de dados.

## Etapas do Projeto

1. **Criação do Projeto Spring**:
   - Nome do projeto: **Rh Queens**.

2. **Configuração da Conexão com o Banco de Dados**:
   - Conexão configurada corretamente para persistir os dados.

3. **Criação do Package Model**:
   - Definição dos atributos para a classe `Funcionario`.
   - Implementação de getters e setters para acessar e modificar os dados.

4. **Criação do Package Repository**:
   - Implementação do repositório usando JPA (Java Persistence API).
   - Usamos o `extends JpaRepository` para facilitar a comunicação com o banco de dados.

5. **Criação dos Endpoints (API RESTful)**:
   - Definição dos atributos para a classe `Funcionario`.
   - Implementação de getters e setters para acessar e modificar os dados.
   - Implementação do repositório usando JPA (Java Persistence API).
   - Criação de endpoints para manipulação de dados.

## Endpoints da API

- **GET** - Buscar todos os funcionários:  
  `GET /funcionarios` → Retorna todos os funcionários cadastrados.

- **GET** - Buscar funcionário por ID:  
  `GET /funcionarios/{id}` → Retorna um funcionário pelo ID.

- **GET** - Buscar funcionário por nome:  
  `GET /funcionarios/nome/{nome}` → Retorna um funcionário pelo nome.

- **POST** - Cadastrar novo funcionário:  
  `POST /funcionarios` → Adiciona um novo funcionário.

- **PUT** - Atualizar funcionário existente:  
  `PUT /funcionarios/{id}` → Atualiza os dados de um funcionário.

- **DELETE** - Excluir funcionário:  
  `DELETE /funcionarios/{id}` → Remove um funcionário do sistema.

## Tecnologias Utilizadas

- **Spring Framework**: Framework principal para desenvolvimento da aplicação.
- **Spring Boot**: Facilita a criação e configuração do projeto Spring.
  - Configuração automática de servidores embutidos (como Tomcat e Jetty) e simplificação da criação de APIs RESTful.
- **JPA (Java Persistence API)**: Usado para mapear objetos Java para tabelas de bancos de dados relacionais.
- **Spring Web**: Facilita a criação de APIs RESTful.
  - Usamos `@RestController` e `@RequestMapping` para definir as rotas e métodos de manipulação de requisições.
- **Insomnia**: Ferramenta de cliente HTTP para testar e depurar APIs RESTful.
  - Embora não seja uma tecnologia de back-end, Insomnia foi essencial para realizar testes das APIs criadas com Spring Boot, validando as requisições GET, POST, PUT, e DELETE.
