# Online Examination System

A Java-based web application developed to manage an **online examination workflow**, including user authentication, test management, question handling, test evaluation, and result management. The project follows a structured Spring Boot application architecture with separate controller, DAO/repository, model, and resource layers.

## Problems It Solves

The project addresses common challenges in conducting and managing online examinations:

- **Manual examination processes:** Provides a web-based platform for conducting examinations digitally.
- **Question management:** Organizes examination questions and test-related information through structured application components.
- **User management:** Provides a dedicated authentication and user-handling layer for the application.
- **Test management:** Supports the organization and processing of online tests.
- **Result management:** Maintains examination results and related information in a structured manner.
- **Centralized data handling:** Separates application logic and data-access operations using a layered architecture.

## Features

- **User Authentication:** Handles user authentication through a dedicated authentication controller.
- **Admin Operations:** Provides a separate controller for administrative functionality.
- **Test Management:** Handles test-related operations through the test controller.
- **Question Management:** Maintains question-related data using dedicated model and repository components.
- **Result Management:** Handles examination result information.
- **User Management:** Maintains user-related data within the application.
- **Web Interface:** Provides web pages using templates and static resources.
- **Layered Architecture:** Separates controllers, data-access components, models, and web resources for better organization.

## Technologies Used

- **Programming Language:** Java
- **Framework:** Spring Boot
- **Frontend:** HTML, CSS, JavaScript
- **Template Engine:** Thymeleaf
- **Database Access:** DAO / Repository Layer
- **Build/Development:** Spring Boot
- **IDE:** IntelliJ IDEA

## Project Structure

```text
OnlineExamSystem/
│
├── src/
│   └── main/
│       ├── java/
│       │   └── ...
│       │       ├── controller/
│       │       │   ├── AdminController.java
│       │       │   ├── AuthController.java
│       │       │   └── TestController.java
│       │       │
│       │       ├── dao/
│       │       │   ├── QuestionRepository.java
│       │       │   ├── ResultRepository.java
│       │       │   ├── UserRepository.java
│       │       │   └── TestRepository.java
│       │       │
│       │       ├── model/
│       │       │   ├── Question.java
│       │       │   ├── Result.java
│       │       │   ├── Test.java
│       │       │   └── User.java
│       │       │
│       │       └── OnlineExamSystemApplication.java
│       │
│       └── resources/
│           ├── static/
│           └── templates/
```

## Application Architecture

The project follows a layered structure where each component has a specific responsibility:

```text
              ┌──────────────────────┐
              │   Web Interface      │
              │ Templates + Static   │
              └──────────┬───────────┘
                         ▼
              ┌──────────────────────┐
              │     Controllers      │
              │ Admin / Auth / Test  │
              └──────────┬───────────┘
                         ▼
              ┌──────────────────────┐
              │    DAO / Repository  │
              │ Question / Result /  │
              │ User / Test          │
              └──────────┬───────────┘
                         ▼
              ┌──────────────────────┐
              │        Models        │
              │ Question / Result /  │
              │ User / Test          │
              └──────────────────────┘
```

## Main Components

### Controllers

The controller layer handles incoming web requests and coordinates application operations.

- `AdminController.java` – Handles administrative operations.
- `AuthController.java` – Handles authentication-related operations.
- `TestController.java` – Handles test-related operations.

### DAO / Repository Layer

The DAO/repository layer is responsible for data-access operations.

- `QuestionRepository.java` – Handles question-related data operations.
- `ResultRepository.java` – Handles result-related data operations.
- `UserRepository.java` – Handles user-related data operations.
- `TestRepository.java` – Handles test-related data operations.

### Model Layer

The model layer represents the main entities used by the application.

- `Question.java`
- `Result.java`
- `Test.java`
- `User.java`

### Resources

The `resources` directory contains the application's web resources:

- **`static/`** – Static frontend resources such as CSS, JavaScript, and other assets.
- **`templates/`** – Server-side HTML templates used to render the application's web pages.

## Project Workflow

The application follows a basic online examination workflow:

```text
User
  │
  ▼
Authentication
  │
  ▼
Test Selection / Test Management
  │
  ▼
Question Handling
  │
  ▼
Online Test
  │
  ▼
Result Processing
  │
  ▼
Result Management
```

## Project Outcome

This project provided practical experience in developing a **Java Spring Boot web application** using a structured layered architecture. It helped build understanding of controllers, repositories/DAO, model classes, server-side templates, web application flow, and separation of application responsibilities.
