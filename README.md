# Prova AV2 - Ecommerce

O projeto está organizado da seguinte maneira:

```css
cssCopiar código
ecommerce/
├── demo/
│   ├── .gitignore
│   ├── HELP.md
│   ├── mvnw
│   ├── mvnw.cmd
│   ├── pom.xml
│   ├── .mvn/
│   │   └── wrapper/
│   │       └── maven-wrapper.properties
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/
│   │   │   │       └── example/
│   │   │   │           └── ecommerce/
│   │   │   │               ├── application/
│   │   │   │               │   └── JwtRestApiApplication.java
│   │   │   │               ├── config/
│   │   │   │               │   └── SecurityConfig.java
│   │   │   │               ├── controller/
│   │   │   │               │   └── AuthController.java
│   │   │   │               ├── model/
│   │   │   │               │   └── LoginRequest.java
│   │   │   │               ├── security/
│   │   │   │               │   └── JwtUtil.java
│   │   │   │               └── service/
│   │   │   │                   └── AuthService.java
│   │   │   └── resources/
│   │   │       └── application.properties
│   │   └── test/
│   │       └── java/
│   │           └── com/
│   │               └── example/
│   │                   └── ecommerce/
│   │                       └── JwtRestApiApplicationTests.java

```

### Descrição dos Arquivos e Diretórios

### Arquivos de Configuração

- **.gitignore**: Arquivo que especifica quais arquivos e diretórios devem ser ignorados pelo sistema de controle de versão Git.
- **HELP.md**: Um arquivo de ajuda que provavelmente contém instruções ou documentação para o projeto.
- **mvnw e mvnw.cmd**: Scripts para executar o Maven Wrapper no Unix e Windows, respectivamente.
- **pom.xml**: Arquivo de configuração do Maven, que define as dependências e plugins do projeto.

### Diretório `.mvn/wrapper`

- **maven-wrapper.properties**: Configurações do Maven Wrapper.

### Diretório `src/main/java/com/example/ecommerce/application`

- **JwtRestApiApplication.java**: Classe principal que inicia a aplicação Spring Boot.

### Diretório `src/main/java/com/example/ecommerce/config`

- **SecurityConfig.java**: Configuração de segurança da aplicação.

### Diretório `src/main/java/com/example/ecommerce/controller`

- **AuthController.java**: Controlador responsável pela autenticação.

### Diretório `src/main/java/com/example/ecommerce/model`

- **LoginRequest.java**: Modelo de dados para requisição de login.

### Diretório `src/main/java/com/example/ecommerce/security`

- **JwtUtil.java**: Utilitário para manipulação de tokens JWT.

### Diretório `src/main/java/com/example/ecommerce/service`

- **AuthService.java**: Serviço responsável pela lógica de autenticação.

### Diretório `src/main/resources`

- **application.properties**: Arquivo de propriedades do Spring Boot, utilizado para configurar a aplicação.

### Diretório `src/test/java/com/example/ecommerce`

- **JwtRestApiApplicationTests.java**: Testes unitários para a aplicação.

### Documentação Detalhada

### `JwtRestApiApplication.java`

<img src= https://github.com/RickRamosss/ecommerce/blob/main/img/Untitled.png>

- Esta é a classe principal que inicia a aplicação Spring Boot usando `SpringApplication.run`.

### `SecurityConfig.java`

<img src= https://github.com/RickRamosss/ecommerce/blob/main/img/Untitled%20(1).png>

- Configura a segurança da aplicação, desabilitando CSRF e permitindo acesso público aos endpoints de autenticação.

### `AuthController.java`

<img src= https://github.com/RickRamosss/ecommerce/blob/main/img/Untitled%20(2).png>

- Controlador que lida com a autenticação. Possui um endpoint `/login` que recebe uma requisição de login e retorna um token JWT.

### `LoginRequest.java`

<img src= https://github.com/RickRamosss/ecommerce/blob/main/img/Untitled%20(3).png>

- Modelo de dados para a requisição de login, contendo `username` e `password`.

### `JwtUtil.java`

<img src= https://github.com/RickRamosss/ecommerce/blob/main/img/Untitled%20(4).png>

- Utilitário para manipulação de tokens JWT, incluindo geração e extração de claims.

### `AuthService.java`

<img src= https://github.com/RickRamosss/ecommerce/blob/main/img/Untitled%20(5).png>

- Serviço que lida com a lógica de autenticação, utilizando `AuthenticationManager` para autenticar as credenciais e `JwtUtil` para gerar tokens JWT.

### Diagrama de fluxo

Com base na análise, o fluxo básico do sistema é:

1. **Inicialização da aplicação** (`JwtRestApiApplication.java`)
2. **Configuração de segurança** (`SecurityConfig.java`)
3. **Recepção de requisição de login** (`AuthController.java`)
4. **Processamento de autenticação** (`AuthService.java`)
5. **Geração de token JWT** (`AuthService.java`)

<img src= (https://github.com/RickRamosss/ecommerce/blob/main/img/ecommerce_auth_flow.png)>



