# Cliente Persona Service

Este microservicio maneja la información de los clientes y personas, permitiendo la creación, consulta y actualización de los datos de los mismos.

## Requisitos

Antes de ejecutar este proyecto, asegúrate de tener instalados los siguientes elementos en tu entorno de desarrollo:

- **Java 17** o superior
- **Maven**
- **Docker**
- **Docker Compose**
- **PostgreSQL** (si no lo ejecutas en un contenedor)

## Configuración de Base de Datos

El servicio requiere una base de datos PostgreSQL. Puedes crear las tablas necesarias usando el archivo `BaseDatos.sql`.

### Pasos para configurar la base de datos:

1. Si tienes PostgreSQL localmente, asegúrate de tener una base de datos llamada `clientePersonaDB` y configúrala en el archivo `application.properties`.

2. Si ejecutas PostgreSQL en un contenedor Docker, puedes usar el siguiente comando:
   ```bash
   docker run --name postgres-clientepersona -e POSTGRES_DB=clientePersonaDB -e POSTGRES_USER=admin -e POSTGRES_PASSWORD=admin -p 5432:5432 -d postgres

Asegúrate de que el Dockerfile esté correctamente configurado.

Construye la imagen de Docker usando Docker Compose:

bash
Copy code
docker-compose build
Inicia los contenedores:

bash
Copy code
docker-compose up
El servicio estará corriendo en el puerto 8081.
