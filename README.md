# FULL_STACK_TASK_MANAGEMENT

# Task Management FRONTEND -

This is a task management web application with a connected backend API. It allows users to register, login, add new tasks, and view their existing tasks. The frontend of the application is built using React, and the backend API is connected using Axios. The project utilizes React Router for navigation and React Toastify for displaying notifications.

## Features

- User Registration: Users can register for a new account using the "Register" page.
- User Login: Existing users can log in using their credentials on the "Login" page.
- Home Page: After login, users are redirected to the home page, where they can view their tasks.
- Add New Task: Authenticated users can add new tasks using the "New Task" page.
- View Tasks: Authenticated users can view all their existing tasks on the "View Tasks" page.
- Toast Notifications: Users receive toast notifications for important actions or events.

## Prerequisites

Before running the application, ensure you have the following:

- Node.js and npm installed on your machine.
- Backend API server running and accessible with the appropriate base URL.

## Getting Started

Follow the steps below to set up and run the Task Management Web App:

1. Clone the repository:

```bash
git clone `https://github.com/saurabhdixit93/FULL_STACK_USER_TASK`
```

2. Change into the project directory:

```bash
cd FULL_STACK_USER_TASK
```

3. Install the project dependencies:

```bash
npm install
```

4. Set the base URL for the backend API:

In the `App.js` file, make sure to set the `REACT_APP_BASE_URL` environment variable to the base URL of your backend API. For example:

```javascript
axios.defaults.baseURL = "http://your-backend-api.com";
```

5. Start the development server:

```bash
npm start
```

The web application will now be accessible in your web browser at `http://localhost:3000`.

## Usage

1. **Register**: Access the web application and click on the "Register" link in the navigation bar. Fill out the registration form with your details and click the "Register" button. You will be redirected to the home page after successful registration.

2. **Login**: If you already have an account, click on the "Login" link in the navigation bar. Enter your login credentials and click the "Login" button. Upon successful login, you will be redirected to the home page.

3. **Home Page**: The home page displays your tasks. If you are not logged in, it will redirect you to the login page. To add a new task, click on the "Add New Task" button.

4. **Add New Task**: Fill out the task details in the form and click the "Add Task" button to create a new task. After adding the task, you will be redirected to the home page.

5. **View Tasks**: Click on the "View Tasks" link in the navigation bar to see all your existing tasks.

6. **Toast Notifications**: You will receive toast notifications for actions such as successful task addition or login failure.

# Task Management Backend -

This is the backend for the Task Management Web Application. It provides the necessary APIs for user authentication and managing tasks. The backend is built using Express.js, MongoDB for the database, and utilizes various middleware for security and logging.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [API Endpoints](#api-endpoints)
  - [User Routes](#user-routes)
  - [Task Routes](#task-routes)
- [Middleware](#middleware)
- [Security](#security)
- [Logging](#logging)
- [Environment Variables](#environment-variables)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Prerequisites

Before running the backend, ensure you have the following:

- Node.js and npm installed on your server or local machine.
- MongoDB database server running and accessible.

## Getting Started

1. Clone the repository:

```bash
git clone https://github.com/saurabhdixit93/FULL_STACK_USER_TASK
```

2. Change into the project directory:

```bash
cd FULL_STACK_USER_TASK
```

3. Install the project dependencies:

```bash
npm install
```

4. Set up the environment variables:

Create a `.env` file in the root of the project and add the following environment variables:

```plaintext
MONGODB_URI=<your-mongodb-connection-string>
FRONT_END_HOME_URL=<your-frontend-home-url>
```

5. Start the backend server:

```bash
npm start
```

The backend server will now be running on the specified port (default is 5000).

## API Endpoints

### User Routes

- **POST /user/sign_up**: Register a new user account.
- **POST /user/login**: Authenticate a user and log them in.

### Task Routes

- **POST /task/:userId/create_task**: Create a new task for a specific user.
- **GET /task/:userId/get_tasks**: Get all tasks for a specific user.
- **GET /task/get_specific_task/:taskId**: Get details of a specific task.
- **PUT /task/update_task/:taskId**: Update details of a specific task.
- **DELETE /task/delete_task/:taskId**: Delete a specific task.

## Middleware

The backend utilizes the following middleware:

- **express.json()**: Parse incoming request bodies in JSON format.
- **express.urlencoded({ extended: true })**: Parse incoming request bodies with URL-encoded data.
- **helmet()**: Sets various HTTP headers to improve security.
- **cors()**: Enables Cross-Origin Resource Sharing (CORS).
- **Custom CORS Middleware**: Adds necessary headers to allow communication with the frontend application.

## Security

- Helmet is used to set secure HTTP headers to mitigate common security risks.

## Logging

- Morgan is used to log HTTP request details in the console and a file (error.log).

## Environment Variables

The backend uses the following environment variables:

- **MONGODB_URI**: Connection string for the MongoDB database.
- **FRONT_END_HOME_URL**: Frontend home URL to set CORS headers properly.

## Contributing

If you wish to contribute to this project, feel free to fork the repository and submit a pull request with your changes.

## License

This project is licensed under the [MIT License](LICENSE).

## Contact

If you have any questions or issues, please contact the project maintainers:

- Maintainer: [Saurabh Dixit](mailto:smartds2550@gmail.com)
- Project Link: [GitHub Repository](https://github.com/saurabhdixit93/FULL_STACK_USER_TASK)
