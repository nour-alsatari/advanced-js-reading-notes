What header(s) are used in authentication and authorization
headers?
The HTTP Authorization request header can be used to provide credentials that authenticate a user agent with a server, allowing access to a protected resource. The Authorization header 

What is safe to put into a JWT? 
The general opinion is that they're good for being used as ID Tokens or Access Tokens and that they're secure - as the tokens are usually signed or even encrypted. You have to remember though, that JWT is not a protocol but merely a message format.

How are JWTs validated?
JWTs are signed so they can't be modified in transit. When an authorization server issues a token, it signs it using a key. When the client receives the ID token, the client validates the signature using a key as well.

Document the following Vocabulary Terms
RBAC:
Role-based access control (RBAC) is a method of restricting network access based on the roles of individual users within an enterprise. RBAC ensures employees access only information they need to do their jobs and prevents them from accessing information that doesn't pertain to them

User Roles: User Roles are permission sets that control access to areas and features within the Professional Archive Platform. Each User account requires a Role assignment.

JWT Token
JSON Web Token is a proposed Internet standard for creating data with optional signature and/or optional encryption whose payload holds JSON that asserts some number of claims. The tokens are signed either using a private secret or a public/private key.