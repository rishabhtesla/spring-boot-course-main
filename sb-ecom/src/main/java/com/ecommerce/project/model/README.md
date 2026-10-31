# Models and Database Relationships

The classes in `model` describe e-commerce data such as products, categories, users, carts, and orders. A class annotated with `@Entity` is mapped by JPA to database storage. Fields describe data, while annotations such as `@Id`, `@ManyToOne`, and `@OneToMany` describe persistence and relationships.

Start with `Product.java`. It has product details and references to its category and seller. Follow the related classes to learn how records connect. Lombok annotations such as `@Data` generate common Java methods during compilation; you will not see those methods written out in the file.

These are persistence models, not necessarily the same shape as API JSON. See the [payload guide](../payload/README.md) for DTOs.

**Practice:** draw the relationship between a product, category, seller, and cart item. Then identify which side stores the foreign key.
