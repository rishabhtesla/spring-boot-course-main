# Tight Coupling

This package demonstrates tight coupling: a class directly depends on a particular implementation. Start with `TightCouplingExample` and follow how `UserManager` obtains or uses its database provider.

The code can work, but changing the provider may require changing the manager too. That makes testing and switching implementations harder. Compare this example with [loose coupling](../../loose/coupling/README.md) and [IoC](../../ioc/coupling/README.md).

**Practice:** identify the exact line where the concrete dependency is chosen. Imagine replacing the database provider and count which classes would need edits.
