# Read07
* Answer the question.
* JWTs Explained.
* Intro to JWT.
* Are JWTs Secure?.

### *Answer the question*
- Q1 : The authorization code is a temporary code that the client will exchange for an access token. 
The code itself is obtained from the authorization server where the user gets a chance to see what 
the information the client is requesting, and approve or deny the request.

- Q2 : Access tokens are the thing that applications use to make API requests on behalf of a user. 
The access token represents the authorization of a specific application to access specific parts of a 
user’s data.

### *JWTs Explained*
- JWT (JSON Web Token) it's an open standard (any one can use it).
- It is used to securely transfer information between any two bodies.(two users , two server).
- It is used because it is digitally signed-information is verified and trusted there is no 
alteration of data in between the transfer.
- It's compact : JWT can be send via URL, POST request, HTTP Header. It's fast transmission .
- Self-contained.
- JWT is usefull (Authentication, Information Exchange).
- JWT structure : Header.Payload.Signature .


For more details watch this [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo).

### *Intro to JWT*
- JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely 
transmitting information between parties as a JSON object. This information can be verified and trusted because 
it is digitally signed.
- When should you use JSON Web Tokens? Authorization, Information Exchange.
- JWT structure :
* Header: The header typically consists of two parts: the type of the token, which is JWT, and the signing 
algorithm being used
* Payload: contains the claims. Claims are statements about an entity (typically, the user) and additional data. 
There are three types of claims: registered, public, and private claims.
* Signature: To create the signature part you have to take the encoded header, the encoded payload, a secret, 
the algorithm specified in the header, and sign that.
![structure](https://cdn.auth0.com/blog/legacy-app-auth/legacy-app-auth-5.png).

For more details see [Intro to JWT](https://jwt.io/introduction/).

### *Are JWTs Secure?*
The contents in a json web token (JWT) are not inherently secure, but there is a built-in feature for 
verifying token authenticity. A JWT is three hashes separated by periods. The third is the signature. 
A public key verifies a JWT was signed by its matching private key.

For more details see [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure).