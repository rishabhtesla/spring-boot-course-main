# Constructor and Setter Injection

This package contains two ways to provide a `Specification` to a `Car`.

- In `constructor/injection`, the constructor requires a `Specification`. The car cannot be created without its required dependency.
- In `setter/injection`, a setter supplies the dependency after the object is constructed.

Both are forms of dependency injection. The matching XML files in `src/main/resources` show how Spring can create the objects and connect them.

**Practice:** compare the constructors and configuration files. Which approach makes it impossible to create an incomplete `Car`? Which one permits replacing the specification later?
