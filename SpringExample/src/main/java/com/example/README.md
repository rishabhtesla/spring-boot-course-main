# Annotation and Autowire Examples

This package groups examples that ask Spring to discover or connect objects using annotations or XML configuration.

- `autowired/annotation` demonstrates Spring annotations for connecting beans.
- `autowire/constructor`, `autowire/name`, and `autowire/type` compare XML autowiring strategies.
- `componentscan` demonstrates finding component classes through scanning; `componentscan/annotation` shows an annotation-based configuration example.

Use the matching XML file under `src/main/resources` when an example loads XML. These are separate demonstrations; run and read one package at a time.

**Practice:** compare one XML wiring example with one annotation example. Find where Spring learns which dependency to give to the class.
