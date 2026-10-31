# API Client

`api.js` creates an Axios client with the backend base URL and shared request settings. Other code can use this client to send requests without repeating the base URL in every feature.

The base URL comes from the `VITE_BACK_END_URL` environment variable, followed by `/api`. Vite only exposes environment variables with the `VITE_` prefix to frontend code. Values included in a frontend build are visible to users, so never put private secrets there.

To understand a feature, find the component or Redux action that calls `api`, note the HTTP method and path, then find the matching Spring controller route in `sb-ecom`.

**Practice:** follow one product-list request from its frontend caller to `ProductController` and compare query parameter names.
