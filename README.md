# REST API - Node.js

Esta es una REST API simple implementada en Node.js utilizando Express. Proporciona operaciones CRUD básicas para gestionar una lista de estudiantes.

## Requisitos

Antes de ejecutar la aplicación, asegúrate de tener lo siguiente instalado:

- Node.js v12 o superior
- npm (Node Package Manager)

## Instalación y Ejecución

### Paso 1: Clonar el Repositorio

Clona este repositorio en tu máquina local:

```bash
git clone https://github.com/tu_usuario/tu_repositorio.git
cd tu_repositorio
```

### Paso 2: Instalar Dependencias

Ejecuta el siguiente comando para instalar las dependencias necesarias:

```bash
npm install
```

### Paso 3: Ejecutar la Aplicación

Inicia el servidor de la API con el siguiente comando:

```bash
node app.js
```

El servidor estará disponible en `http://localhost:80/`.

## Endpoints Disponibles

### Raíz
- **GET** `/`
  Devuelve un mensaje de bienvenida: `Node JS api`.

### Estudiantes

- **GET** `/api/students`
  Devuelve una lista de todos los estudiantes.

- **GET** `/api/students/:id`
  Devuelve los detalles de un estudiante por su ID.
  - **Respuesta de Error**: 404 si el estudiante no se encuentra.

- **POST** `/api/students`
  Agrega un nuevo estudiante. Requiere un cuerpo JSON con las siguientes propiedades:
  ```json
  {
    "name": "Nombre del estudiante",
    "age": "Edad del estudiante",
    "enroll": "true/false"
  }
  ```

- **DELETE** `/api/students/:id`
  Elimina un estudiante por su ID.
  - **Respuesta de Error**: 404 si el estudiante no se encuentra.

## Archivos Importantes

- **`app.js`**: Contiene la lógica principal de la API.

## Contribución

Si deseas contribuir a este proyecto, por favor, realiza un fork del repositorio, haz tus cambios y abre un Pull Request.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.
