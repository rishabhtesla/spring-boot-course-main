# Store, Actions, and Reducers

The Redux store keeps shared state that multiple components need. In this application, that includes product, cart, authentication, order, payment, admin, and seller state.

`reducers/store.js` combines the feature reducers and restores some initial values from `localStorage`. A reducer describes how a piece of state changes. Actions are dispatched to request those changes; components can read state from the store through React Redux.

Follow one feature through three parts: the component that dispatches or reads state, the action logic (often in `actions`), and the matching reducer. Check persistence behavior carefully before changing authentication or cart data.

**Practice:** trace adding an item to the cart. Identify what event dispatches the action and what state field changes.
