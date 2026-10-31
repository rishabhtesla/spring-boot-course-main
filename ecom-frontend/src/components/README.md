# React Components

Components are reusable pieces of a React page. Most files here export a component function that returns JSX. A page may be built from smaller components, such as a product grid containing product cards.

The folders group related screens and widgets: `home`, `products`, `cart`, `checkout`, `auth`, `admin`, and `shared`. `shared` contains UI pieces reused across multiple screens. `App.jsx` connects many of these components to URL routes.

When reading a component, find its inputs (props), local state, event handlers, and child components. Then follow any data request to the [API client](../api/README.md) or shared state to the [store](../store/README.md).

**Practice:** open the products page component and trace how one product becomes a visible card. Change a harmless label or empty-state message and observe the page.
