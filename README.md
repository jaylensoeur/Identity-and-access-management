# Identity-and-access-management
Identity and Access Management

## OAuth 2.0 

- OAuth 2.0 enables applications to request for authorisation and obtain an access token to access the resources of an API.
- OAuth 2.0 enables control over API authorisations for consumers
- Scopes are used to control the access a consumer has to resources
- OAuth 2.0 specification defined four grant types
     
     **Authorization code** grant type with Proof Key for Code Exchange (PKCE, pronounced pixie) can be used by:
     * traditional web applications,
     * public applications,
     * as well as native applications
    
    **Implicit** grant type is not recommended to obtain an access token with the default response mode as it exposes the access     token to potential compromise.
  
     **Password** grant type is best restricted to legact user migration cases as it exposes user credentials to an application.
  
     **Client Credentials** grant type is for API request where the application owns the request resource.

- A refresh token is used to obtain a new access token when the old access token expires
