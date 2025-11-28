# n8n Starter Kit (PostgreSQL + Docker)

Este repositorio contiene una configuración lista para usar de **n8n** (herramienta de automatización de flujos de trabajo) utilizando **Docker** y **PostgreSQL** como base de datos backend. Está diseñado para facilitar el despliegue rápido y seguro de n8n en tu propia infraestructura.

## 🚀 Características

- **n8n**: Última versión estable de la plataforma de automatización.
- **PostgreSQL**: Base de datos robusta para producción (reemplaza a SQLite por defecto).
- **Docker Compose**: Orquestación de contenedores simplificada.
- **Persistencia de Datos**: Volúmenes configurados para n8n y PostgreSQL.
- **Configuración Flexible**: Variables de entorno centralizadas en `.env`.

## 📋 Prerrequisitos

Antes de comenzar, asegúrate de tener instalado:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- Git

## 🛠️ Instalación y Uso

1.  **Clonar el repositorio**
    ```bash
    git clone <URL_DEL_REPOSITORIO>
    cd n8n-starter-main
    ```

2.  **Configurar variables de entorno**
    Revisa el archivo `docker/.env` y ajusta los valores según tus necesidades (zona horaria, credenciales, etc.).
    ```bash
    # Ejemplo de contenido en docker/.env
    TZ=America/Bogota
    DB_POSTGRESDB_PASSWORD=tu_password_seguro
    ```

3.  **Iniciar los servicios**
    Ejecuta el siguiente comando desde la raíz del proyecto para levantar n8n y PostgreSQL:
    ```bash
    docker compose -f docker/docker-compose.postgres.yml --env-file docker/.env up -d
    ```

4.  **Acceder a n8n**
    Abre tu navegador y visita:
    [http://localhost:5678](http://localhost:5678)

## 📂 Estructura del Proyecto

```
n8n-starter-main/
├── docker/
│   ├── .env                       # Variables de entorno
│   └── docker-compose.postgres.yml # Configuración de Docker Compose
├── docs/                          # Documentación detallada
│   ├── 01-que-es-n8n.md
│   ├── 03-instalacion-docker.md
│   └── ...
└── README.md                      # Este archivo
```

## 📚 Documentación

Para más detalles sobre configuración, seguridad y uso avanzado, consulta la carpeta `docs/`:

- [¿Qué es n8n?](docs/01-que-es-n8n.md)
- [Arquitectura](docs/02-arquitectura.md)
- [Instalación con Docker](docs/03-instalacion-docker.md)
- [Configuración de PostgreSQL](docs/04-postgresql.md)
- [Seguridad](docs/08-seguridad.md)

## 🤝 Contribución

Si deseas contribuir, por favor abre un issue o envía un Pull Request.

## 📄 Licencia

Este proyecto está bajo la licencia [MIT](LICENSE) (o la que corresponda).
