Aprendendo Spring

Descrição

Este é um projeto de estudo em Spring Boot, implementando um CRUD de usuários com autenticação JWT. O objetivo é demonstrar boas práticas no desenvolvimento de APIs REST.

Tecnologias Utilizadas

Java (Spring Boot)
Spring Security (Autenticação com JWT)
Spring Data JPA (Persistência de dados)
Banco de dados (PostgreSQL)
Maven (Gerenciador de dependências)
Estrutura do Projeto

AprendendoSpring/ │-- src/main/java/com/diego/aprendendospring/ │ ├── business/ # Regras de negócio │ │ └── UsuarioService.java │ ├── controller/ # Controllers da API │ │ ├── UsuarioController.java │ │ └── dtos/ # Objetos de Transferência (DTOs) │ │ └── UsuarioDTO.java │ ├── infrastructure/ │ │ ├── entity/ # Entidades do banco │ │ │ ├── Usuario.java │ │ │ ├── Endereco.java │ │ │ └── Telefone.java │ │ ├── repository/ # Repositórios JPA │ │ │ ├── UsuarioRepository.java │ │ │ ├── EnderecoRepository.java │ │ │ └── TelefoneRepository.java │ │ ├── security/ # Configuração JWT │ │ │ ├── JwtUtil.java │ │ │ ├── JwtRequestFilter.java │ │ │ ├── SecurityConfig.java │ │ │ └── UserDetailsServiceImpl.java │ │ ├── exceptions/ # Tratamento de exceções │ │ │ ├── ConflictException.java │ │ │ └── ResourceNotFoundException.java │ ├── AprendendoSpringApplication.java # Classe principal │-- src/main/resources/ │ ├── application.properties # Configurações │-- pom.xml # Dependências do projeto

Como Rodar o Projeto

Clone este repositório: git clone https://github.com/seu-usuario/aprendendo-spring.git

Entre na pasta do projeto: cd aprendendo-spring

Configure o banco de dados no application.properties

Compile e rode o projeto com Maven: mvn spring-boot:run

Endpoints da API

Método	Endpoint	Descrição
POST	/usuarios	Criar um usuário
GET	/usuarios/{id}	Buscar um usuário pelo ID
PUT	/usuarios/{id}	Atualizar um usuário
DELETE	/usuarios/{id}	Remover um usuário
Autenticação JWT

O projeto implementa autenticação via JWT. Para acessar as rotas protegidas:

Autentique-se via POST /auth/login e obtenha um token.
Envie o token no cabeçalho Authorization: Bearer nas requisições.
Contribuição

Sinta-se livre para abrir issues e enviar pull requests para melhorias!

Licença

Este projeto está sob a licença MIT.
