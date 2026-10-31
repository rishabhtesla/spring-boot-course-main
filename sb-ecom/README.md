# sb-ecom: The E-commerce Backend

This is the largest Java project in the repository. It provides API features for products, categories, users, addresses, carts, orders, analytics, and payments. Read it after the small REST API projects so the folder and framework names are familiar.

## Run requirements

The Maven configuration declares Java 24, Spring Boot, Spring Data JPA, PostgreSQL, Spring Security, JWT, Stripe, validation, and OpenAPI dependencies. Before running, install a compatible JDK and PostgreSQL, then review `src/main/resources/application.properties` and set the required local configuration. Do not commit credentials, JWT signing keys, or payment secrets.

From this directory:

```bash
./mvnw spring-boot:run
```

Run tests with:

```bash
./mvnw test
```

Springdoc is included for API documentation. After starting the application, try `http://localhost:8080/swagger-ui/index.html`; if it is unavailable, check the app's startup logs and configuration.

## Learn the architecture

An API request usually travels through these layers:

```text
Browser or API client
    -> controller (HTTP route and request)
    -> service (application rules)
    -> repository (database operations)
    -> model/entity (stored data)
```

Data transfer objects (DTOs) and response classes shape the data sent over the API. They help keep the external API separate from database entities.

Use the [ProductController example](src/main/java/com/ecommerce/project/controller/README.md) as your first trace: find a product endpoint, follow it into the service interface and implementation, then follow repository and model usage. Read [payloads and DTOs](src/main/java/com/ecommerce/project/payload/README.md) to understand the request and response types.

## Suggested study order

1. [Configuration and application startup](src/main/java/com/ecommerce/project/config/README.md)
2. [Models and database relationships](src/main/java/com/ecommerce/project/model/README.md)
3. [Repositories](src/main/java/com/ecommerce/project/repositories/README.md)
4. [Payloads and DTOs](src/main/java/com/ecommerce/project/payload/README.md)
5. [Services and business logic](src/main/java/com/ecommerce/project/service/README.md)
6. [Controllers and HTTP APIs](src/main/java/com/ecommerce/project/controller/README.md)
7. [Exceptions and error responses](src/main/java/com/ecommerce/project/exceptions/README.md)
8. [Authentication and security](src/main/java/com/ecommerce/project/security/README.md)
9. [Utilities](src/main/java/com/ecommerce/project/util/README.md)

## Practice by building

Start with a small, read-only endpoint or a simple field. Trace the existing feature end-to-end before making a change. Then add validation, a service operation, a repository query if needed, a controller route, and a frontend call. Leave payment flows and authorization changes until you understand how the existing security rules work.

## Continue

The React user interface lives in [ecom-frontend](../ecom-frontend/README.md). Learn its routes and API client after you can explain a backend request from controller to database.
