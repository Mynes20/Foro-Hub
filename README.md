# ForoHub

Es una API REST desarrollada con Spring Framework para gestionar un foro de discusión. Los usuarios pueden crear, leer, actualizar y eliminar tópicos (CRUD). La API está diseñada siguiendo las mejores prácticas del modelo REST, e incluye validaciones, autenticación/autorización y una base de datos relacional para la persistencia de la información.

##  Características

- 📝 Crear un nuevo tópico
- 📖 Mostrar todos los tópicos creados
- 🔍 Mostrar un tópico específico
- ✏️ Actualizar un tópico
- 🗑️ Eliminar un tópico
- ✔️ Validaciones de las reglas de negocio
- 🔒 Autenticación y autorización de usuarios

## Tecnologías Utilizadas

- **Java 11**
- **Spring Boot**
- **Spring Data JPA**
- **Spring Security**
- **Hibernate**
- **H2 Database** (para desarrollo y pruebas)
- **MySQL** (para producción)
- **Maven**

### Prerrequisitos

- JDK 11 o superior
- Maven
- MySQL (para entorno de producción)

##  Uso de la API

- **Crear un nuevo tópico**
    ```http
    POST /api/topics
    ```
    - Cuerpo de la petición (JSON):
        ```json
        {
            "titulo": "Título del Tópico",
            "mensaje": "Contenido del Tópico",
            "autorId": 1
        }
        ```

- **Mostrar todos los tópicos**
    ```http
    GET /api/topics
    ```

- **Mostrar un tópico específico**
    ```http
    GET /api/topics/{id}
    ```

- **Actualizar un tópico**
    ```http
    PUT /api/topics/{id}
    ```
    - Cuerpo de la petición (JSON):
        ```json
        {
            "titulo": "Nuevo Título del Tópico",
            "mensaje": "Nuevo Contenido del Tópico"
        }
        ```

- **Eliminar un tópico**
    ```http
    DELETE /api/topics/{id}
    ```

### Autenticación y Autorización

La API usa Spring Security para la autenticación y autorización. Los usuarios deben autenticarse para acceder a los endpoints. 

### Validaciones

- Todos los campos son obligatorios al crear o actualizar un tópico.
- Los mensajes de error se devuelven en caso de fallos en las validaciones.

## Autor

- Mynor Garcia
