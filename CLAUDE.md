# Slowle — Claude Config

## Project Overview

**Slowle** is a Spring Boot web application built with a Vaadin frontend.

- **Group:** `com.mbarydev`
- **Artifact:** `Slowle`
- **Package:** `com.mbarydev.slowle`

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Java 21 |
| Framework | Spring Boot 4.0.5 |
| Frontend | Vaadin 25.1.2 |
| Persistence | Spring Data JPA + Spring Data JDBC |
| HTTP Client | Spring RestClient |
| Web | Spring Web MVC |
| Utilities | Lombok |
| Build | Maven (Maven Wrapper included) |

## Key Commands

```bash
# Run the application
./mvnw spring-boot:run

# Run tests
./mvnw test

# Build (skip tests)
./mvnw package -DskipTests

# Build frontend assets (Vaadin)
./mvnw vaadin:build-frontend
```

## Project Structure

```
src/
  main/
    java/com/mbarydev/slowle/   # Application source code
    resources/
      application.yaml          # App configuration
  test/
    java/com/mbarydev/slowle/   # Tests
```

## Conventions

- Use Lombok annotations (`@Data`, `@Builder`, `@RequiredArgsConstructor`, etc.) to reduce boilerplate.
- Vaadin views live in `com.mbarydev.slowle` (or a `ui`/`views` subpackage).
- Configuration goes in `application.yaml`, not `application.properties`.
- Prefer constructor injection over field injection.
