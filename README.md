# nodejs-generic-api

## Overview

This project is a **Generic MVC Architecture Node.js API** designed as a template to teach programming concepts to individuals new to software development. It provides a foundational structure for building APIs using the Model-View-Controller (MVC) design pattern, making it easier to understand and implement scalable and maintainable applications.

## Technologies Used

This project leverages the following technologies:

- **Node.js**: A JavaScript runtime for building fast and scalable server-side applications.
- **Express.js**: A minimal and flexible Node.js web application framework for handling HTTP requests and routing.
- **Knex.js**: A SQL query builder for Node.js, used for database interactions.
- **SQLite**: A lightweight, serverless database for development and testing purposes.

## Project Structure

The project follows a modular and organized structure based on the MVC (Model-View-Controller) pattern:

```
Node.js-Generic-API/
├── LICENSE
├── package.json
├── README.md
├── src/
│   ├── routes.js                # Defines the API routes and their handlers
│   ├── server.js                # Entry point of the application
│   ├── app/
│   │   ├── controllers/         # Contains controller logic
│   │   │   └── GeneralController.js
│   │   ├── errors/              # Custom error handling classes
│   │   │   └── ApplicationError.js
│   │   └── models/              # Database models
│   │       └── GeneralModel.js
│   ├── config/
│   │   ├── db.js                # Database connection setup
│   │   └── knexfile.js          # Knex.js configuration file
│   └── shared/
│       └── Util.js              # Shared utility functions
```

### Key Components

1. **`server.js`**: The main entry point of the application. It initializes the Express server and sets up middleware and routes.

2. **`routes.js`**: Defines the API endpoints and maps them to the appropriate controller methods.

3. **Controllers**: Located in the `src/app/controllers/` directory, controllers handle the business logic of the application. For example, `GeneralController.js` contains the logic for general API operations.

4. **Models**: Found in the `src/app/models/` directory, models interact with the database. `GeneralModel.js` is an example of a model that defines how data is structured and accessed.

5. **Error Handling**: The `src/app/errors/` directory contains custom error classes, such as `ApplicationError.js`, to handle application-specific errors.

6. **Configuration**: The `src/config/` directory includes configuration files for the database connection (`db.js`) and Knex.js (`knexfile.js`).

7. **Utilities**: The `src/shared/` directory contains reusable utility functions, such as `Util.js`, to avoid code duplication.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/LuccaSabbatini/Node.js-Generic-API.git
   cd Node.js-Generic-API
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up the database:
   - Update the database configuration in `src/config/knexfile.js` if needed.
   - Run migrations to set up the database schema:
     ```bash
     npx knex migrate:latest --knexfile src/config/knexfile.js
     ```

### Running the Application

1. Start the development server:

   ```bash
   npm start
   ```

2. The API will be available at `http://localhost:3000` by default.

### Testing the API

You can use tools like [Postman](https://www.postman.com/) or [cURL](https://curl.se/) to test the API endpoints defined in `src/routes.js`.

## Purpose

This project was created as a **template project** to teach programming concepts to beginners. It demonstrates how to structure a Node.js application using the MVC architecture, making it easier for new developers to understand the separation of concerns and best practices in software development.

Feel free to use this project as a starting point for your own applications or as a learning resource to deepen your understanding of Node.js and API development.
