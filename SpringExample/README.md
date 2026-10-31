# SpringExample: Objects, IoC, and Dependency Injection

This project contains small, separate examples of how Java objects can work together and how Spring can create and connect those objects. It uses Spring Framework directly rather than Spring Boot, so some examples are started from their own `main` classes.

## Concepts in plain language

- An **object** is a running instance of a class. A `Car` object can hold a `Specification` object.
- **Coupling** describes how dependent one class is on the details of another. Tight coupling makes a class difficult to change; loose coupling makes alternatives easier to provide.
- An **interface** describes behavior that multiple classes can provide.
- **Dependency injection** means giving an object the other objects it needs, instead of making it construct every dependency itself.
- **Inversion of Control (IoC)** means handing responsibility for creating and connecting objects to a framework or container.
- A **Spring bean** is an object managed by Spring.

## Where to look

| Example area | What to compare |
|---|---|
| `com/tight/coupling` | A manager that creates or directly depends on a specific provider |
| `com/loose/coupling` | A manager that depends on a shared provider interface |
| `com/ioc/coupling` | The provider is supplied to the manager, making the dependency replaceable |
| `car/example/constructor/injection` | A constructor receives a `Specification` |
| `car/example/setter/injection` | A setter supplies a dependency after object creation |
| `com/example/autowired` and `com/example/autowire` | Annotation-based and XML-based wiring examples |
| `com/example/componentscan` | How component scanning lets Spring find annotated classes |
| `src/main/resources/*.xml` | XML configuration examples that describe beans and dependencies |

The directories demonstrate alternative approaches. Read a complete example within one directory at a time; similarly named classes in different packages are separate examples, not duplicate files that must be combined.

## Run and inspect an example

This project does not include the Maven wrapper. Use an installed Maven command to compile it:

```bash
mvn test
```

The project has no test classes yet, so use the examples' `App` or `*Example` main classes to see their output. In an IDE, import this directory as a Maven project, open one of the example main classes, and run it. The constructor-injection example is a good starting point: run `car.example.constructor.injection.App`, then inspect its `Car` and `Specification` classes.

The XML and Spring-managed examples need their matching XML configuration on the classpath. Run the main class in the same example package and note which configuration file it loads; do not combine unrelated examples.

## A simple reading exercise

In the constructor-injection example, `Car` cannot be constructed without a `Specification`. The constructor makes that requirement visible. If a different `Specification` implementation is passed, the `Car` can use it without knowing how it was created.

## Practice

1. Find the tight-coupling example and identify which class chooses the concrete data provider.
2. Compare that with the loose-coupling example. Identify the interface and the class that supplies its implementation.
3. Change the provider in the IoC example without rewriting the manager.
4. Compare constructor injection with setter injection. Which dependency is required to create the object?
5. Find the XML bean definition that connects two classes, then locate those classes in Java.

## Next

Continue to [media](../media/README.md), where the same ideas form a small database-backed REST API.
