# Models

Models describe the application's data. The classes in this folder are also used as JPA entities, which means they can be mapped to database tables.

Read `SocialUser`, `SocialProfile`, `SocialGroup`, and `Post`. Look for fields, `@Entity`, ID annotations, and relationship annotations. A relationship tells JPA how records in different tables are connected.

When a controller returns an entity, Spring can serialize its fields as JSON. Database relationships and JSON object relationships are not always the same thing, so inspect the actual response rather than assuming every related object is returned.

**Practice:** identify which class owns each relationship and draw a small diagram of the entities before changing a relationship.
