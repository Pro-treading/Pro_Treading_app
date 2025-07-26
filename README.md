# Pro_Treading_app

A Spring Boot application for user management and two-factor authentication, built as part of my dream project.

## Features

- User registration and authentication
- Two-factor authentication (2FA) support
- Role-based access control (e.g., customer, admin)
- RESTful API endpoints
- MySQL database integration
- Secure password handling

## Technologies Used

- Java 17+
- Spring Boot
- Spring Data JPA (Hibernate)
- Lombok
- MySQL
- Maven
- HTML
- CSS
- JavaScript

## Project Structure

```
src/
  main/
    java/
      com/
        ProTreading/
          controller/
            HomeController.java      # REST API controller for home endpoint
          Modal/
            User.java               # User entity with 2FA and role
            TwoFactorAuth.java      # Embedded class for 2FA settings
          domain/
            USER_ROLE.java          # Enum for user roles
    resources/
      application.properties        # Application configuration (ignored in .gitignore)
```

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven
- MySQL database

### Setup

1. **Clone the repository:**
   ```sh
   git clone https://github.com/Pro-treading/Pro_Treading_app.git
   cd Pro_Treading_app
   ```

2. **Configure the database:**
   - Create a MySQL database (e.g., `yt_treading`).
   - Update `src/main/resources/application.properties` with your DB credentials.
   - **Note:** The real `application.properties` is ignored for security. Use `application.properties.example` as a template if provided.

3. **Build and run the application:**
   ```sh
   mvn clean install
   mvn spring-boot:run
   ```

4. **Access the API:**
   - Home endpoint: [http://localhost:5455/](http://localhost:5455/)

## Key Classes

- **User.java**  
  Represents a user entity with fields for name, email, password (write-only), 2FA settings, and role.

- **TwoFactorAuth.java**  
  Embedded in `User`, stores 2FA status and method.

- **USER_ROLE.java**  
  Enum for user roles (e.g., `ROLE_CUSTOMER`, `ROLE_ADMIN`).

- **HomeController.java**  
  REST controller with a welcome endpoint.

## Security

- Passwords are write-only in






