# Don't do: 

1. Using long-living access tokens
2. Using the client credentials grant type to implement functionality that accesses user resources
3. Registering the same client credentials in multiple apps
4. Send sensitive data in the JWT token
	- Lead to Compromising sensitive information in client and outside of Https protection
5. Send too much data in the JWT token
	- Performance issue with creating signature for token and verifying it in the resource server
7. Disabling the CSRF protection on the Authorization Server
6. Using symmetric key pairs to issue and validate the JWT tokens
	- it lead to breaking the least privilege principle
8. Using blackboarding for the token validation
9. Implementing a custom OAuth2 functionality
10. Using unsigned JWT tokens without introspection
