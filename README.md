# REST API - Node.js

This is a simple REST API implemented in Node.js using Express. Provides basic CRUD operations to manage a list of students.

## Requirements

Before running the app, make sure you have the following installed:

- Node.js v12 or higher
- npm (Node Package Manager)

## Installation and Execution

### Step 1: Clone the Repository

Clone this repository to your local machine:

```bash
git clone https://github.com/JordinPinzon/my-rest-api.git
cd my-rest-api
```

### Step 2: Install Dependencies

Run the following command to install the necessary dependencies:

```bash
npm install
```

### Step 3: Run the Application

Start the API server with the following command:

```bash
node app.js
```

The server will be available at `http://localhost:80/`.

## Available Endpoints

### Root
- **GET** `/`
  Returns a welcome message: `Node JS api`.

### Students

- **GET** `/api/students`
  Returns a list of all students.

- **GET** `/api/students/:id`
  Returns the details of a student by their ID.
  - **Error Response**: 404 if the student is not found.

- **POST** `/api/students`
  Add a new student. Requires a JSON body with the following properties:
  ```json
  {
    "name": "Student name",
    "age": "Student's age",
    "enroll": "true/false"
  }
  ```

- **DELETE** `/api/students/:id`
  Delete a student by their ID.
  - **Error Response**: 404 if the student is not found.

## Important Files

- **`app.js`**: Contains the main logic of the API.

## Contribution

If you want to contribute to this project, please fork the repository, make your changes and open a Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
