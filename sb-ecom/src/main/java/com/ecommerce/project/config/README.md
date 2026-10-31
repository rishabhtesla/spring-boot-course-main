# Configuration and Application Startup

`SbEcomApplication` is the starting point. Its `main` method calls `SpringApplication.run`, which starts Spring Boot and creates the application context: the place where Spring finds and manages application components.

The `config` package contains shared configuration classes and constants. `AppConstants` holds values reused in more than one place, such as default pagination settings. `WebMvcConfig` and `SwaggerConfig` customize web/API behavior.

Configuration values that vary by machine, such as database credentials or payment credentials, belong in local configuration or environment variables rather than committed source code. Review `src/main/resources/application.properties` before launching.

**Practice:** trace a pagination default from `AppConstants` to a controller query parameter and explain how a caller can override it.
