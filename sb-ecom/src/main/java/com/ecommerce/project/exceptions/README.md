# Exceptions and API Errors

Exceptions represent problems while an operation is running. `ResourceNotFoundException` can describe a missing record; `APIException` represents an application-level API problem. `MyGlobalExceptionHandler` centralizes how selected exceptions become HTTP error responses.

This lets controllers and services report a meaningful problem without repeating the same response-building code everywhere. When you add an error case, follow existing exception types and handler behavior so the API stays consistent.

**Practice:** trace what happens when a product is not found. Identify where the exception is raised and how the handler shapes the response.
