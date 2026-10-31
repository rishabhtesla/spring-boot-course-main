# Repositories

A repository is the database-access layer. `SocialUserRepository` and the other interfaces build on Spring Data JPA repository types, so Spring can provide common database operations such as saving and finding records.

Follow a repository call from `SocialService`. The service decides what operation is needed; the repository performs the persistence work. This separation keeps HTTP details out of database code.

**Practice:** find a repository method used by a service, then identify the model type and ID type in its declaration. Add a query method only after checking whether Spring Data can derive it from the method name.
