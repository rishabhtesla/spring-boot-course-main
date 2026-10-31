# FirstSpring: Your First Web API

This is the first stop in the learning path. It is a small Java and Spring Boot application with three `/hello` endpoints. The goal is to understand what a web server does and how Java code turns a request into a response.

## Start with these words

- **Java** is the programming language used to write the classes in `src/main/java`.
- A **class** is a named description of data and behavior. `HelloController` is a class that contains methods for handling web requests.
- A **method** is a named block of code. `hello()` is a method inside `HelloController`.
- An **HTTP request** is a message a client (such as a browser) sends to a server. A response is the server's reply.
- A **REST endpoint** is an address and HTTP method that the application understands.
- **JSON** is a text format often used to exchange data between a server and a browser.
- **Spring Boot** starts and configures the web server so you can focus on the application code.

## Run it

From this directory, run:

```bash
./mvnw spring-boot:run
```

Open `http://localhost:8080/hello` in a browser. Try `http://localhost:8080/hello/Ada` too. To stop the server, press `Ctrl+C` in the terminal.

To run the tests:

```bash
./mvnw test
```

## Read the code in this order

1. `src/main/java/com/embarkx/FirstSpring/FirstSpringApplication.java` starts the Spring Boot application.
2. `HelloController.java` maps HTTP requests to Java methods.
3. `HelloResponse.java` holds the message that Spring converts into a JSON response.
4. `src/main/resources/application.properties` is the application's configuration file.

In `HelloController`, `@RestController` tells Spring that this class handles web requests and returns response data. `@GetMapping("/hello")` connects a GET request to a method. `@PathVariable` takes a value from the URL, so `/hello/Ada` passes `"Ada"` to the method. `@PostMapping` handles a POST request, and `@RequestBody` reads data sent in that request.

## Follow one request

When you visit `/hello/Ada`, Spring matches the URL to `helloParam`. The method receives `"Ada"`, creates a `HelloResponse`, and returns it. Spring turns that Java object into JSON, similar to:

```json
{"message":"Hello, Ada"}
```

The exact response can be checked in your browser's developer tools or with an HTTP client.

## Practice

1. Change the greeting in `hello()` and run the app again.
2. Add a method that responds to `/hello/{name}/welcome`.
3. Add a field to `HelloResponse` and observe how the JSON response changes.
4. Explain in your own words the difference between `@GetMapping` and `@PostMapping`.

## Next

Continue to [SpringExample](../SpringExample/README.md) to learn how Spring creates and connects Java objects.
