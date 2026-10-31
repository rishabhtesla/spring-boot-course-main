# Utilities

Utility classes hold small pieces of shared behavior that do not belong to one controller. `AuthUtil` provides authentication-related helper behavior used elsewhere in the application.

When reading a helper, find its callers first. That shows what assumptions it makes and which part of the application depends on it. Keep business workflows in services rather than turning a utility class into a place for unrelated operations.

**Practice:** search for `AuthUtil` usages and trace one call to see which user or authentication information it provides.
