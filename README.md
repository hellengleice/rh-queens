# Documentação Super Já 

**Link do Repositório**: [https://github.com/abilafora/superJa](https://github.com/abilafora/superJa)  
**Link do Banco de Dados**: [https://superja.onrender.com](https://superja.onrender.com)

---

## Projeto: Aplicativo de Delivery 

### Integrantes:
- [Abiqueila de Souza](https://github.com/Abilafora/) 
- [Evelyn Pereira](https://github.com/EvelynSantos6) 
- [Hellen Gleice](https://github.com/hellengleice) 
- [Isabela Santos](https://github.com/Isabela-prog) 
- [Maytê Araújo](https://github.com/maytearaujo) 
- [Thainara Cruz](https://github.com/ThainaraCruz) 

---

### Objetivo: 
O **SuperJá** é um aplicativo de delivery elaborado para realizar entregas de compras feitas em supermercados. Ele permite o **cadastro de usuários**, o **gerenciamento de produtos** e a **associação com as categorias dos produtos**.

---

### 1. Packages Utilizados: 

- **Model**: Representa os dados (Produto, Usuario, Categoria).
- **Controller**: Controlador para manipulação das requisições (ControllerProduto, ControllerUsuario, ControllerCategoria).
- **Repository**: Camada responsável pela comunicação com o banco de dados (RepositoryProduto, RepositoryUsuario, RepositoryCategoria).
- **Service**: Camada responsável pela regra de negócio.
- **Security**: Camada responsável pela segurança da aplicação.

---

### Etapas do Projeto:

#### Pacote: model 
Contém as classes de modelo que representam as entidades do banco de dados.

- **Usuario** 
  - Atributos: `id`, `nome`, `usuário (e-mail)`, `foto`, `senha`.
  - Relacionamento: Um usuário pode ter vários produtos.

- **UsuarioLogin** 
  - Atributos: `id`, `nome`, `usuário (e-mail)`, `foto`, `senha`, `token`.
  - Relacionamento: Cada usuário possui um token único para login no sistema.

- **Produto** 
  - Atributos: `id`, `nomeProduto`, `estoque`, `preco`, `validade`.
  - Relacionamento: Cada produto pertence a uma categoria e pode estar relacionado com vários usuários.

- **Categoria** 
  - Atributos: `id`, `setor`.
  - Relacionamento: Uma categoria pode ter vários produtos associados.

#### Pacote: repository 
Contém os repositórios responsáveis pela persistência de dados usando Spring Data JPA.

- **UsuarioRepository**: Interface para manipulação de dados de usuários.
- **ProdutoRepository**: Interface para manipulação de dados de produtos.
- **CategoriaRepository**: Interface para manipulação de dados de categorias.

#### Pacote: controller 
Contém as classes responsáveis por expor as funcionalidades com os endpoints REST.

- **UsuarioController**: Define endpoints para cadastro, atualização e consulta de usuários.
- **ProdutoController**: Define endpoints para cadastro, atualização, consulta e exclusão de produtos.
- **CategoriaController**: Define endpoints para cadastro, atualização e consulta de categorias.

#### Pacote: service 
Contém a lógica de negócios, como validações e regras específicas.

- **UsuarioService**: Contém a lógica de validação do cadastro de usuário, garantindo que o usuário será cadastrado apenas após autenticação.
- **ProdutoService**: Contém a lógica de negócios onde o produto recebe um desconto de 10% quando o preço for maior que R$ 50,00.

#### Pacote: security 
Contém a camada responsável pela segurança da aplicação. Através do usuário (e-mail) e senha, será verificado se o usuário possui permissão para acessar o sistema.

**O ecossistema de segurança é composto por 5 classes**:

- **UserDetailsServiceImpl** 
- **UserDetailsImpl** 
- **JwtService** 
- **JwtAuthFilter** 
- **BasicSecurityConfig** 

---

### Endpoints 

#### 1. UsuarioController

- **GET /usuarios/logar**  
  Permite que o usuário acesse o sistema.
  
- **GET /usuarios/all**  
  Retorna todos os usuários cadastrados.
  
- **GET /usuarios/{id}**  
  Retorna um usuário específico pelo ID.
  
- **POST /usuarios/cadastrar**  
  Cria um novo usuário (somente mulheres).
  
- **PUT /usuarios/atualizar**  
  Atualiza os dados de um usuário.

#### 2. ProdutoController

- **GET /produtos**  
  Retorna todos os produtos cadastrados.
  
- **GET /produtos/{id}**  
  Retorna um produto específico pelo ID.
  
- **GET /produtos/nomeProduto/{nomeProduto}**  
  Retorna produtos filtrados pelo nome do produto.
  
- **POST /produtos**  
  Cria um novo produto associando-o a uma categoria e a um usuário.
  
- **PUT /produtos**  
  Atualiza os dados de um produto.
  
- **DELETE /produtos/{id}**  
  Exclui um produto pelo ID.

#### 3. CategoriaController

- **GET /categorias**  
  Retorna todas as categorias cadastradas.
  
- **GET /categorias/{id}**  
  Retorna uma categoria específica pelo ID.
  
- **GET /categorias/setor/{setor}**  
  Filtra categoria pelo setor.
  
- **POST /categorias**  
  Cria uma nova categoria.
  
- **PUT /categorias**  
  Atualiza os dados de uma categoria.
  
- **DELETE /categorias/{id}**  
  Exclui uma categoria pelo ID.

---

### Validações 

#### Cadastro de Produto
A criação de um produto exige que os dados estejam corretos, como o preenchimento obrigatório dos campos `nomeProduto`, `estoque`, `preco` e `validade`.  
Caso o produto cadastrado tenha um preço maior que R$ 50,00, receberá um **desconto de 10%**.

---

### Tecnologias Utilizadas 

- **Spring Framework**: Framework principal para desenvolvimento da aplicação.
- **Spring Boot**: Facilita a criação e configuração do projeto Spring. Configuração automática de servidores embutidos (como Tomcat e Jetty) e simplificação da criação de APIs RESTful.
- **JPA (Java Persistence API)**: Usado para mapear objetos Java para tabelas de bancos de dados relacionais.
- **Spring Web**: Facilita a criação de APIs RESTful. Usamos **@RestController** e **@RequestMapping** para definir as rotas e métodos de manipulação de requisições.
- **Insomnia**: Ferramenta de cliente HTTP para testar e depurar APIs RESTful.
- **MySQL**: Banco de dados relacional utilizado para persistir os dados dos funcionários.
- **Swagger**: Ferramenta que fornece suporte para documentação automatizada da API, geração de código e testes.

---

### Como Executar o Projeto 

**Pré-requisitos**:

- **Java 17 ou superior**: O projeto utiliza o Spring Boot 2.x.
- **IDE (como STS)**: Para editar e rodar o projeto.
- **Maven**: Para gerenciar as dependências do projeto.
