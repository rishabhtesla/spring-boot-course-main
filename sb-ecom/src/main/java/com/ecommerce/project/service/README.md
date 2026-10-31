# Services and Business Logic

The service layer carries out application operations. Interfaces such as `ProductService` describe what can be done; classes such as `ProductServiceImpl` implement those operations using repositories and other services.

Start with `ProductService` and `ProductServiceImpl`. Follow `addProduct` or a product search. Notice that a service may validate or transform data, call a repository, and return a DTO. The controller handles HTTP details; the service handles the work requested by that endpoint.

**Practice:** trace one method from its service interface to its implementation, note each repository call, and draw the input/output types. Then add a small service operation before wiring it to a new route.
