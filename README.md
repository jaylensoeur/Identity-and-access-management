# Identity and Access Management

## OAuth 2.0 

- OAuth 2.0 enables applications to request for authorisation and obtain an access token to access the resources of an API
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

## OpenID Connect

- Provides an identity layer on top of OAuth 2.0 to authenticate users
- Enables single sign-on (SSO)
- Provides an ID Token and UserInfo endpoint to obtain user profile info
- Defines a set of standard claims that can be obtained about a user
- Allows for the use of additional, custom claims
- Defined three grant flows for different client profiles
- Provides several options for returning an authorisation code and/or security tokens via front-channel or back-channel response
- Returning access tokens or refresh tokens via front-channel responses should be avoided by using a back-channel response or alternate response mode
- Returning sensitive information in ID Tokens via front-channel responses should be avoided by using a back-channel response or the UserInfo endpoint or encrypting the ID Token if encryption is support

## SAML
- SAML is an XML-based framework for exchaning security information between business partners
- Provided two features which became widely used:
          * cros-domain SSO 
          * identity federation
- A SAML service provider delegates use authentication to an identity provider
- A SAML identity provider authenticated a user and returns the results of a user authentication even in an XML message called an authentication response
- An authentication response contains an authentication assertion with claims about the authnetication event and authenticated user
- Identity federation establishes a common identitifer for a user between an identity provider and a service provider
- Businesss customers of applications often want to use their corporate identity providers to authenticate their users to applications
- New applications should consider using an authentication broker service or SAML library to simplify the task of supporting SAML

## Single Sign On (SSO)
- SSO is the ability for a user to authenticate once and access multiple applications that delegate authentication to the same identity provider without the user re authneticating to each application
- SSO with an identity provider avoids exposure of user credentials to applications
- The use of an identity provider may relieve developers of the work to build login pages and account recovery mechanisms is each application
- The use of an identity provider for SSO provides a single place to administer authentication policy and a single account shut-off point
- SSO can create a single point of failure if not designed to be highly available as well as secure
- Identity providers should be configured with session settings appropriate for the applications relying on the identity provider

## Mitigating Risks
- Processes should be analysed for vulnerabilities
- Train users to recognise and avoid phishing attacks to reduce risk of malware
- Use Multi-factor authentication to mitigate the risk of compromised passwords
- Monitor for software vulnerabilities and apply patches when vulnerabilities are announced
- Follow secure configuration guidelines for all cloud-hosted components such as Amazon S3 buckets
- Encrypt sensitive data at rest and in transit, including backups and log files
- Avoid storing cleartext passwords
- Provide security training for developers
- Vet partners by checking certifications and conducting due diligence evaluation of security practices
- Mitigate the risk of insider threat by granting minimum needed privileges and frequently reviewing access grant as well as logs
