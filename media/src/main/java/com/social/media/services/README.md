# Services

The service layer contains operations that the application offers. `SocialService` connects the controller to repositories and can coordinate more than one database operation.

When reading a service method, ask:

1. What input did the controller pass in?
2. Which repository methods are called?
3. What object or result is returned to the controller?
4. What should happen when the requested data is missing?

This project keeps the service code compact so you can see the layer boundaries. Follow a service method together with the corresponding controller and repository.

**Practice:** add a service method for finding one user and decide how a missing user should be represented.
