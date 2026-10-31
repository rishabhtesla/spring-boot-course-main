# Authentication and Security

This package contains authentication and authorization code. **Authentication** asks who a caller is; **authorization** asks what that caller is allowed to do. Spring Security applies rules to incoming requests, and JWT (JSON Web Token) code supports sending signed identity information with requests.

Read the pieces in this order:

1. `request/` contains login and signup input classes.
2. `AuthController` and the authentication service handle authentication operations.
3. `services/UserDetailsServiceImpl` loads user information for Spring Security.
4. `jwt/JwtUtils` creates or checks tokens; `AuthTokenFilter` reads a token from a request.
5. `WebSecurityConfig` and `WebConfig` define security and web behavior.

Do not treat a frontend-only route check as security. The backend must enforce permissions. Never share real JWT signing keys, passwords, or tokens.

**Practice:** follow the login request into the backend response, then determine how a later request carries its token and which backend component checks it. Avoid changing security rules until you can explain the complete path.
