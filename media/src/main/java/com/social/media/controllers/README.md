# Controllers

A controller is the web-facing entry point for an API feature. `SocialController` uses `@RestController` to mark the class as a REST controller and mapping annotations to connect HTTP requests to Java methods.

Start with `SocialController.java`:

- `@GetMapping("/social/users")` handles a request to read users.
- `@PostMapping("/social/users")` reads a request body and creates a user.
- `@DeleteMapping("/social/users/{userId}")` takes an ID from the URL using `@PathVariable`.
- `ResponseEntity` lets the method return both a response body and an HTTP status such as `200 OK` or `201 Created`.

The controller delegates to `SocialService` instead of implementing database operations itself. Trace each method into the service to see the next layer.

**Practice:** add a route to get one user by ID. Keep URL/request handling in the controller and ask the service to perform the lookup.
