# Read02
* Answer the question.
* An introduction to NodeJS and Express
* What is NPM?
* What is TDD?
* CI/CD

### *Answer the question*
- Q1 :
| put |  PATCH     | 
| :---: | :---: |
| PUT is a method of modifying resource where the client sends data that updates the entire resource .| PATCH is a method of modifying resources where the client sends partial data that is to be updated without modifying the entire data. |
| In a PUT request, the enclosed entity is considered to be a modified version of the resource stored on the origin server, and the client is requesting that the stored version be replaced|With PATCH, however, the enclosed entity contains a set of instructions describing how a resource currently residing on the origin server should be modified to produce a new version.|
| HTTP PUT is said to be idempotent, So if you send retry a request multiple times, that should be equivalent to a single request modification|  HTTP PATCH is basically said to be non-idempotent. So if you retry the request N times, you will end up having N resources with N different URIs created on the server.|
| It has High Bandwidth | 	Since Only data that need to be modified if send in the request body as a payload , It has Low Bandwidth|

- Q2 : Nock, MockServer,Beeceptor

- Q3 : Developers describe apiDocjs as "Inline Documentation for RESTful web APIs". It creates a documentation f
rom API annotations in your source code. It includes a default template which uses handlebars, Bootstrap, 
RequireJS and jQuery for the output of the generated apidata.js and apiproject.js as a html-page. On the other 
hand, Swagger Codegen is detailed as "*Generate API clients or server stubs for REST API *". It is an open 
source project which allows generation of API client libraries (SDK generation), server stubs, and 
documentation automatically from an OpenAPI Specification.

- Q4 :
- SOAP stands for Simple Object Access Protocol whereas REST stands for Representational State Transfer.
- SOAP is a protocol whereas REST is an architectural pattern.
- SOAP uses service interfaces to expose its functionality to client applications while REST uses Uniform  Service locators to access to the components on the hardware device.
- SOAP needs more bandwidth for its usage whereas REST doesn’t need much bandwidth.
- Comparing SOAP vs REST API, SOAP only works with XML formats whereas REST work with plain text, XML, HTML and JSON.
- SOAP cannot make use of REST whereas REST can make use of SOAP.

### *An introduction to NodeJS and Express*
- Node (or more formally Node.js) is an open-source, cross-platform runtime environment that allows developers 
to create all kinds of server-side tools and applications in JavaScript. The runtime is intended for use 
outside of a browser context (i.e. running directly on a computer or server OS). As such, the environment omits 
browser-specific JavaScript APIs and adds support for more traditional OS APIs including HTTP and file system 
libraries.
- Express is the most popular Node web framework, and is the underlying library for a number of other popular 
Node web frameworks.

For more details see [An introduction to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction).

### *What is NPM?*

npm is the world's largest software registry. Open source developers from every continent use npm to share and borrow packages, and many organizations use npm to manage private development as well.

npm consists of three distinct components:
- the website
- the Command Line Interface (CLI)
- the registry

For more details see [What is NPM?](https://docs.npmjs.com/about-npm).

### *What is TDD?*

“Test-driven development” refers to a style of programming in which three activities are tightly interwoven: coding, testing (in the form of writing unit tests) and design (in the form of refactoring).

For more details see [What is TDD](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1)).


### *CI/CD*

npm is the world's largest software registry. Open source developers from every continent use npm to share and 
CI/CD is a method to frequently deliver apps to customers by introducing automation into the stages of app 
development. The main concepts attributed to CI/CD are continuous integration, continuous delivery, and 
continuous deployment.

For more details see [What is NPM?](https://www.youtube.com/watch?v=xSv_m3KhUO8).