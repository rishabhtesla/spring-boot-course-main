# Inversion of Control

In this example, a dependency is supplied to the object that needs it instead of being selected internally. This is a basic form of Inversion of Control (IoC): the code that uses a dependency does not own every decision about creating it.

Read `UserManager` and its providers, then inspect `applicationIoCLooseCouplingExample.xml` to see how Spring's container can connect beans. Compare the result with [tight coupling](../../tight/coupling/README.md) and [loose coupling](../../loose/coupling/README.md).

**Practice:** locate the XML bean definitions and explain which object is created and which dependency is passed into it.
