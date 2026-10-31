# ecom-frontend: The React User Interface

This project is the browser-based frontend for the e-commerce application. It uses JavaScript, React, Vite, React Router, Redux Toolkit, and Axios. The frontend and backend are separate programs: the frontend displays pages and sends HTTP requests to the backend API.

## Concepts in plain language

- **JavaScript** is the programming language used by the browser code.
- **React** builds a page from reusable components. A component is usually a JavaScript function that returns UI.
- **JSX** is the HTML-like syntax used inside React components.
- **State** is data that can change and cause the page to update.
- **Routing** selects which page to show for a URL.
- **Redux** keeps shared application state, such as login and cart data, in one store.
- **Axios** sends HTTP requests to the backend.
- **Vite** runs the development server and builds the frontend for release.

## Run it

Install Node.js, then from this directory run:

```bash
npm ci
npm run dev
```

Vite prints a local URL in the terminal, usually `http://localhost:5173`. To create a production build, run `npm run build`. To check the code with ESLint, run `npm run lint`.

The API client in `src/api/api.js` reads `VITE_BACK_END_URL` from the frontend environment and appends `/api`. Set that variable in a local environment file if required; do not commit secrets. The backend also needs to be running for API-backed pages to load their data.

## Suggested study order

1. [Routes and pages](src/App.jsx) — see how URLs select screens.
2. [Components](src/components/README.md) — learn the reusable UI building blocks.
3. [API client](src/api/README.md) — see how the frontend calls the backend.
4. [Store and reducers](src/store/README.md) — understand shared state and actions.
5. [Hooks](src/hooks/README.md) and [utilities](src/utils/README.md) — learn reusable behavior.

Start with a public product page before examining checkout, payments, or admin screens.

## Follow one feature

Choose a screen in `src/App.jsx`, open its component, and identify the data it needs. Follow where that data is requested or read from the Redux store, then find where the result is rendered. For an API call, inspect `api.js` and compare the URL and data with the corresponding backend controller.

## Practice

1. Change a visible label and see Vite update the page.
2. Follow the products route into the `Products` component.
3. Find how a product list is loaded and identify the API endpoint it calls.
4. Add a small UI state change, such as a button that expands or collapses a short message.
5. After understanding the backend route, change one display field without changing authentication or payment behavior.
