# launcher

![Diagrama de flujo](https://github.com/test-propital/launcher/blob/main/microservicios.drawio.png)

## Architecture Overview

Esta es una aplicación de microservicios dividida en submódulos o que sigue un enfoque de repositorios múltiples (multi-repo). Cada servicio está aislado en su propio submódulo o repositorio individual, permitiendo un desarrollo y despliegue independiente.

El proyecto incluye diferentes microservicios que se comunican entre sí mediante tecnologías como NATS para mensajería y Redis, que se utiliza específicamente para gestionar la persistencia y la conexión de websockets. Esta configuración permite una gestión eficiente de sesiones y mensajes en tiempo real dentro de la arquitectura distribuida. Cada servicio puede ser escalado, desplegado y mantenido de manera autónoma.

## Tech Stack

El stack tecnológico principal para esta aplicación de microservicios incluye:

- **Node.js**: Runtime JavaScript utilizado para construir el backend.
- **NestJS**: Framework progresivo para aplicaciones Node.js, utilizado para la estructura y desarrollo de microservicios.
- **Express**: Framework web minimalista utilizado en algunos servicios para manejar peticiones HTTP.
- **Docker**: Para contenerizar los servicios y facilitar el despliegue.
- **Kubernetes**: Orquestrador de contenedores utilizado para gestionar y escalar los microservicios.
- **NATS**: Sistema de mensajería que permite la comunicación entre microservicios.
- **Redis**: Usado para persistencia de datos en tiempo real y como un broker para websockets.
- **PostgreSQL**: Base de datos relacional para el almacenamiento de datos estructurados.
- **MongoDB**: Base de datos NoSQL utilizada para almacenar datos no estructurados.
- **TypeScript**: Lenguaje de programación que extiende JavaScript con tipado estático.
- **GCP (Google Cloud Platform)**: Proveedor de infraestructura en la nube utilizado para alojar y gestionar los microservicios en entornos de producción.
 
## dev

1. clonar el repositorio
2. clonar los submodulos con el comando  "git submodule update --init --recursive"
3. crear un .env basado en el .env.templated
4. ejecutar el comando  `docker compose up --build`

