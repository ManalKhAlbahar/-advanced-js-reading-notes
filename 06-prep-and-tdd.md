# Read06
* Answer the question.
* Securing Passwords.
* Basic Auth.
* OWASP auth cheatsheet.
* bcrypt docs .

### *Answer the question*
- Q1 : A singleton is a class that allows only a single instance of itself to be created and gives 
access to that created instance. It contains static variables that can accommodate unique and private 
instances of itself. It is used in scenarios when a user wants to restrict instantiation of a class 
to only one object. This is helpful usually when a single object is required to coordinate actions 
across a system.
The singleton pattern is used in programming languages such as Java and .NET to define a global 
variable. A single object used across systems remains constant and needs to be defined only once 
rather than many times.

- Q2 : True
- Q3 : Middleware could be built as so when a set of parameters are requested within a webpage it 
bypasses a response cycle and overlay’s a set of data.

### *Securing Passwords*

Passwords are the first line of defense against cyber criminals. It is the most vital secret of every 
activity we do over the internet and also a final check to get into any of your user account, whether 
it is your bank account, email account, shopping cart account or any other account you have.

Cryptographic hash algorithms MD5, SHA1, SHA256, SHA512, SHA-3 are general purpose hash functions, 
designed to calculate a digest of huge amounts of data in as short a time as possible. Hashing is the 
greatest way for protecting passwords and considered to be pretty safe for ensuring the integrity of 
data or password.
-PROBLEMS WITH CRYPTOGRAPHIC HASH ALGORITHM:
- 1- Brute Force attack
- 2- Hash Collision attack

For more details see [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html).

### *Basic Auth*
basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user 
name and password when making a request. In basic HTTP authentication, a request contains a header 
field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of 
ID and password joined by a single colon.

For more details see [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication).

### *OWASP auth cheatsheet.*
Authentication :is the process of verifying that an individual, entity or website is whom it claims 
to be.

Session Management: is a process by which a server maintains the state of an entity interacting with 
it. This is required for a server to remember how to react to subsequent requests throughout a 
transaction.
- Authentication General Guidelines:
User IDs:Make sure your usernames/user IDs are case-insensitive. 
Email address as a User ID.
-Implement Proper Password Strength Controls:
- Password Length:
Minimum length of the passwords should be enforced by the application. Passwords shorter than 8 
characters are considered to be weak.
Maximum password length should not be set too low.

INCORRECT AND CORRECT RESPONSE EXAMPLES:
Login
- Incorrect response examples:
- 1)"Login for User foo: invalid password."
- 2) "Login failed, invalid user ID."
- 3) "Login failed; account disabled."
- 4) "Login failed; this user is not active."
- Correct response example:
"Login failed; Invalid user ID or password."

- Account Lockout:
The most common protection against these attacks is to implement account lockout, which prevents any 
more login attempts for a period after a certain number of failed logins.


For more details see [OWASP auth cheatsheet.](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html).

### *bcrypt docs *
node.bcrypt.js: A library to help you hash passwords.
- Security Issues And Concerns:
- An issue with passwords was found with a version of the Blowfish algorithm developed for John the 
Ripper. This is not present in the OpenBSD version and is thus not a problem for this module. HT 
zooko.
- Versions < 5.0.0 suffer from bcrypt wrap-around bug and will truncate passwords >= 255 characters 
leading to severely weakened passwords.
- Versions < 5.0.0 do not handle NUL characters inside passwords properly leading to all subsequent 
characters being dropped and thus resulting in severely weakened passwords.

Install via NPM: npm install bcrypt.

For more details see [bcrypt docs.](https://www.npmjs.com/package/bcrypt).


