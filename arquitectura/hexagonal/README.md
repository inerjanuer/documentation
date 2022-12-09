### Estructura de proyecto con arquitectura hexagonla
Estructura de un proyecto desarrollado en java con arquitectura hexagonal.


.
└── proyecto/
    ├── src/
    │   ├── main/
    │   │   └── package/
    │   │       ├── domain/
    │   │       │   ├── model (entidades)/
    │   │       │   │   └── UserEntity.java
    │   │       │   ├── port  (puertos de salida)/
    │   │       │   │   └── IUserPort.java
    │   │       │   └── exception (excepciones de entidades)/
    │   │       │       ├── enum/
    │   │       │       │   └── EntityMessage.java
    │   │       │       └── EntityException.java
    │   │       ├── application/
    │   │       │   ├── usecase (puertos de entrada)/
    │   │       │   │   └── IUserUseCase.java
    │   │       │   ├── service   (implementacion del caso de uso)/
    │   │       │   │   └── UserService.java
    │   │       │   └── exception (excepciones de negocio)/
    │   │       │       ├── enum/
    │   │       │       │   └── BusinessMesage.java
    │   │       │       └── BusinessException.java
    │   │       └── infraestructure/
    │   │           ├── dto ( datos de entrada)/
    │   │           │   └── UserDTO.java
    │   │           ├── adapters/
    │   │           │   ├── input (controladores) /
    │   │           │   │   └── UserController.java
    │   │           │   └── output (peticiones de salida, sql, aws, ...)/
    │   │           │       └── UserAdapter.java
    │   │           ├── jpa (jpa implementacion sql)/
    │   │           │   ├── UserJPA.java 
    │   │           │   └── UserMapper.java
    │   │           ├── repository ( reposotorio consultas sql) /
    │   │           │   └── UserRepository.java
    │   │           ├── util ( codigo general para implementacion)/
    │   │           │   └── AdapterOperation.java
    │   │           ├── config (configuracion general de aplicacion)/
    │   │           │   ├── BeanConfiguration.java
    │   │           │   └── SwaggerConfiguration.java
    │   │           └── exception (excepciones tecnicas )/
    │   │               ├── enum/
    │   │               │   └── TechnicalMessage.java
    │   │               └── TechnicalException.java
    │   └── test/
    │       └── package
    └── pom.xml