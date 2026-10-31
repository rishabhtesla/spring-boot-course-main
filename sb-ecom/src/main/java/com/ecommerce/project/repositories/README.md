# Repositories

Repositories are Spring Data interfaces for database operations. For example, `ProductRepository` extends `JpaRepository<Product, Long>`, which provides common operations for `Product` records whose IDs are `Long` values.

Some method names, such as `findByCategoryOrderByPriceAsc`, describe queries that Spring Data can generate. `JpaSpecificationExecutor` also allows more flexible searches. Follow repository calls from a service to understand when and why they are used.

**Practice:** find a product lookup in `ProductServiceImpl`, locate the repository method it calls, and identify the returned type. Notice how `Page` and `Pageable` support pagination.
