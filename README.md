# Proyecto Spring Boot con Maven

Este proyecto es una API REST desarrollada con Spring Boot y Maven. Su objetivo es proporcionar dos endpoints que permiten saludar a los usuarios mediante diferentes tipos de parámetros en las solicitudes HTTP.

## Requisitos previos

Para ejecutar este proyecto, necesitas:

- Tener instalado [Java](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- Tener instalado [Maven](https://maven.apache.org/install.html)
- Crear un proyecto en [Spring Initializr](https://start.spring.io/)
- Importar el proyecto en un entorno de desarrollo como [IntelliJ IDEA](https://www.jetbrains.com/idea/) o [Eclipse](https://www.eclipse.org/downloads/)

## Configuración

El servidor está configurado para ejecutarse en el puerto 9000. Esto se especifica en el archivo `application.properties`:

```properties
server.port=9000
```

## Endpoints

### GET `/helloWorld` (RequestParam)

- Recibe el parámetro `name` como un RequestParam opcional.
- Si no se proporciona, el valor por defecto es "UNKNOWN".
- Ejemplo de uso:
    - `http://localhost:9000/helloWorld`
    - `http://localhost:9000/helloWorld?name=myName`

### GET `/helloWorld2` (PathVariable)

- Recibe el parámetro `name` como un PathVariable opcional.
- Si no se proporciona, el valor por defecto es "UNKNOWN".
- Ejemplo de uso:
    - `http://localhost:9000/helloWorld2`
    - `http://localhost:9000/helloWorld2/myName`

## Comandos básicos de Maven

Para ejecutar el proyecto en tu entorno local, clónalo y usa los siguientes comandos:

- **Compilar el proyecto:**
  ```sh
  mvn compile
  ```
- **Empaquetar el proyecto:**
  ```sh
  mvn package
  ```
- **Limpiar el proyecto:**
  ```sh
  mvn clean
  ```
- **Ejecutar la aplicación:**
  ```sh
  mvn spring-boot:run
  ```

