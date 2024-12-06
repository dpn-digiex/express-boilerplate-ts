# Express Boilerplate with TypeScript

This project serves as a boilerplate for building RESTful APIs using **Express.js** with **TypeScript**. It includes a structured folder hierarchy, OpenAPI documentation, and reusable components for faster development and maintenance.

## Features

- **TypeScript Support:** Type-safe code for improved developer experience.
- **API Documentation:** Built-in OpenAPI integration for generating and serving API documentation.
- **Modular Structure:** Separation of concerns with folders for controllers, models, services, and routers.
- **Testing:** Dedicated folder structure for tests with test files for different layers of the application.
- **Common Utilities:** Shared middleware, models, and utilities for reusability.
- **Husky Integration:** Pre-commit hooks to enforce code quality standards.
- **Prettier Integration:** Prettier for consistent code formatting.
- **ESLint Integration:** ESLint for linting the code.

---

## Folder Structure

### Root
- **.husky/**: Contains Git hooks for pre-commit and other lifecycle events.
- **.env**: Environment variables configuration file.
- **Dockerfile**: Configuration for containerizing the application.
- **tsconfig.json**: TypeScript compiler configuration.
- **vite.config.mts**: Configuration for building the project using Vite.

---

### `/src`
Main source folder for the application.

#### `/api`
Contains all API-related modules.

- **healthCheck/**: Placeholder for health check endpoints.
- **user/**: Example module for user-related operations.
  - `userController.ts`: Handles incoming requests and responses for user endpoints.
  - `userModel.ts`: Defines the data structure (e.g., database models) for users.
  - `userRepository.ts`: Handles data access logic (e.g., database queries) for users.
  - `userRouter.ts`: Defines route handlers for user endpoints.
  - `userService.ts`: Implements business logic for user operations.
  
- **api-docs/**: Handles OpenAPI documentation.
  - `openAPIDocumentGenerator.ts`: Generates the OpenAPI specification.
  - `openAPIResponseBuilders.ts`: Utility to build consistent API responses.
  - `openAPIRouter.ts`: Serves the OpenAPI specification as an endpoint.

---

#### `/common`
Contains shared resources used across the application.

- **middleware/**: Reusable middleware for request/response handling.
- **models/**: Shared data models used across modules.
- **utils/**: Utility functions for common operations.

---

#### Root Files
- **index.ts**: Entry point for the application.
- **server.ts**: Initializes and configures the Express server.

---

#### Prerequisites
- **Node.js** (>= 16.x)
- **Docker** (optional, for containerized deployments)
