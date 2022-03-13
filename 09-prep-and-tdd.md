# Read09 :Authorization/Authentication

### *Answer the question*
- Q1 :The HTTP headers Authorization header is a request type header that used to contains the credentials information to authenticate a user 
through a server. If the server responds with 401 Unauthorized and the WWW-Authenticate header not usually.

Authenticate response headers define the authentication method that should be used to gain access to a resource. They must specify which 
authentication scheme is used, so that the client that wishes to authorize knows how to provide the credentials.

- Q2 : A JWT is URL-encoding-safe. There will be no data-loss when used in-place; no additional encoding is required; it is even URL encoding safe 
inherently, applying url-encoding (percentage-encoding) on the JWT multiple times will not destroy it.
This safety is limited: There can be a data-leak when used in-place if the URL itself is part of such a data-leak. By how URLs are commonly in 
use, you should treat any JWT in an URL query parameter as-if the data-leak already happened and therefore prepared the JWT for it already (e.g. 
prevent replay attacks).And it will be at best as safe as the transport of the URL information is, and never more safe.And if the transport of the 
URL information is not safe, everything in the URL can never be more safe either, which includes the JWT when used as a GET parameter.

- Q3:It is composed of JSON objects, which are base64url-encoded and joined together as a string separated by dots. Anyone in possession of JWT 
can decode it and see the content. JWT tokens are digitally signed (the signature part) using the payload content and a secret key. In order to 
change the content, the secret key is required to generate the signature again, otherwise, the signature will be invalid. When a token is posted 
to the server, it must be validated to check if anyone has tempered the token or not. Lack of proper validation can cause serious security issues 
and here we will see how to properly validate a JWT.


### *RBAC*
Role-based access control (RBAC), also known as role-based security, is an access control method that assigns permissions to end-users based on 
their role within your organization. RBAC provides fine-grained control, offering a simple, manageable approach to access management that is less 
error-prone than individually assigning permissions. 

### *User Roles*

a role is a semantic construct that you use for building permissions. A role could be defined by any number of criteria including authority, 
responsibilities, cost center, and business unit.
The role, essentially, refers to the collection of user permissions. This is different from the traditional groups, which are a collection of 
users. In the context of RBAC, permissions are tied to roles rather than being directly connected to identities.
Roles are more stable than groups because roles are organized around access management, and in a typical organization, functions and activities 
don’t change as frequently as identities do.

### *JWT Token*

A JSON Web Token (JWT) is an access token standardized according to RFC 7519, which makes it possible for two parties to securely exchange data. 
It contains all important information about an entity, meaning that no database queries are necessary and the session doesn’t need to be saved on 
the server.