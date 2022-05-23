# Read34:   API Integration
* Review API Server Build .
* Review Auth Server Build .

### *Review API Server Build(RBAC)*

- Dynamic API Server : An Express/Node.js based server designed to be a “model agnostic” REST API server, which can perform CRUD operations on any data model

- Support all REST/HTTP methods:

1. GET: Retrieve record(s) from a data source
    - All
    - One (by id)
    - Some (by filtering)
2. POST: Create a new record in a data source
3. PUT: Update a single full record in a data source
4. PATCH: Update part of a single record in a data source
5. DELETE: Delete a record in a data source

- Obey a standard output format:
1. Results will be returned in JSON format
2. Results will be served with the correct HTTP header - application/json
3. The GET Route, when not retrieving by ID, must return a full header, with count ,pages, and a results array
4. All other routes must return a single object, representing the state of the entity following the operation

For more details see [Review API Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/api-server/).

### *Review Auth Server Build*

- Authentication Server / Module : An Express/Node.js based server using a custom “authentication” module that is designed to handle 
user registration and sign in using Basic, Bearer, or OAuth along with a custom “authorization” module that will grant/deny users 
access to the server based on their role or permissions level.

- The system to be built will have the following core features:

1. Users can create an account, associated with a “role”
2. User Roles will be pre-defined and will each have a list of allowed capabilities
      - admin can read, create, update, delete
      - editor can read, create, update
      - writer can read, create
      - user can read
3. Users can then login with a valid username and password
4. Alternatively, users can login using an OAuth provider such as Google or GitHub
     - In this case, users should be automatically assigned the role of user
5. Once logged in, Users can then access any route on the server, so long as they are permitted by the capabilities that match their role.
     - For example, a route that deletes records should only work if your user role is “admin”



For more details see  [Review Auth Server Build](https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/auth-server/).

