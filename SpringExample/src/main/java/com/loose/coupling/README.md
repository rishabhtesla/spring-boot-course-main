# Loose Coupling

This package demonstrates loose coupling. `UserManager` depends on the `UserDataProvider` interface rather than requiring one specific provider class. The database and web-service providers can offer the same behavior through that interface.

An interface is a promise about available operations. Code that depends on the promise does not need to know which implementation will fulfill it. Compare this package with [tight coupling](../../tight/coupling/README.md) and [IoC](../../ioc/coupling/README.md).

**Practice:** find both provider implementations and compare their `UserDataProvider` behavior. Explain why the manager can work with either one.
