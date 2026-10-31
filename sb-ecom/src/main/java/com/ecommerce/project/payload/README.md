# Payloads, DTOs, and Responses

An API payload is the data sent in an HTTP request or response. A DTO (Data Transfer Object) is a Java class designed to carry that API data. Classes here include product, category, cart, order, and user DTOs, along with response wrappers.

Why not send database entities directly? DTOs let the API choose which fields clients can send or see, and let the database model evolve separately. Annotations such as `@Valid` on a controller parameter trigger validation rules declared on the DTO.

Follow a product endpoint from its request DTO to the response DTO. Look for where the service maps between the DTO and the `Product` entity; ModelMapper is included as a dependency.

**Practice:** compare `Product` with `ProductDTO`. List fields they share and fields that appear only in one. Explain why an API might intentionally omit a database field.
