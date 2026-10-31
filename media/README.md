# media: A Small Database-Backed REST API

This project is a compact example of a Spring Boot API for social users, profiles, groups, and posts. It is useful for seeing how a request can pass through a controller, service, repository, and database model.

## What you will learn

- **REST API:** named URLs receive HTTP requests and return data.
- **Controller:** translates a web request into a call to application logic.
- **Service:** holds the application's operations and coordinates work.
- **Repository:** provides database access without writing basic SQL for every operation.
- **Entity/model:** a Java class that represents data stored in a database.
- **JPA:** a Java standard that maps objects to relational database records.
- **H2:** an in-memory database dependency useful for local learning.

## Run it

From this directory:

```bash
./mvnw spring-boot:run
```

The project includes H2 as its runtime database dependency. Check `src/main/resources/application.properties` for the active database and server settings before changing them. To run the tests:

```bash
./mvnw test
```

The controller exposes `GET /social/users`, `POST /social/users`, and `DELETE /social/users/{userId}`. Use an HTTP client to try the POST and DELETE requests. The request body for POST must be JSON that matches the `SocialUser` model.

## Trace a request

Start with `controllers/SocialController.java`. Its `GET /social/users` method calls `SocialService`; follow that call into `services/SocialService.java`, then into the repository interface in `repositories`. The returned `SocialUser` objects are serialized into JSON by Spring.

Read `models` after you understand the request flow. Model relationships connect the social user, profile, group, and post data.

## Practice

1. Add a GET endpoint for finding one user by ID.
2. Follow the existing delete operation and explain what happens if the ID does not exist.
3. Add one simple field to a model and observe how it is represented in the database and response.
4. Add a validation rule to user input and test both valid and invalid requests.

## Code-area guides

- [Controllers](src/main/java/com/social/media/controllers/README.md)
- [Models](src/main/java/com/social/media/models/README.md)
- [Repositories](src/main/java/com/social/media/repositories/README.md)
- [Services](src/main/java/com/social/media/services/README.md)

## Next

Continue to [sb-ecom](../sb-ecom/README.md) to explore the same layers in a much larger application.
