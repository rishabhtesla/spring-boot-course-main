# Controllers and HTTP APIs

Controllers connect HTTP URLs to application code. `@RestController` marks a class as a REST controller and `@RequestMapping("/api")` adds a shared URL prefix. Mapping annotations such as `@GetMapping`, `@PostMapping`, `@PutMapping`, and `@DeleteMapping` connect HTTP methods to Java methods.

Begin with `ProductController`. A public products request can include query parameters for search, category, page, and sorting. The controller calls `ProductService` and wraps its result in `ResponseEntity` with an HTTP status.

Common request inputs:

- `@PathVariable`: a value inside the URL, such as `{productId}`.
- `@RequestParam`: an optional or required URL query value, such as `?pageNumber=0`.
- `@RequestBody`: data sent in the request body, often JSON.
- `@Valid`: asks Spring to check declared validation constraints.

**Practice:** use the public product route, then find its method in `ProductController` and trace the service call. Add a query parameter only after deciding how the service should use it.
