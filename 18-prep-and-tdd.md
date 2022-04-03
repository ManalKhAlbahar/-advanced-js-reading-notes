# Read18 : AWS: API, Dynamo and Lambda
* AWS API Gateway Overview
* AWS API Gateway.
* AWS DynamoDB Guide.
* AWS DynamoDB.
* Dynamoose.

### *AWS API Gateway Overview*
- Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect 
those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API 
requests.

- API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing 
them to the correct backends. It provides a set of tools that help you manage your API definitions and the mappings between endpoints and 
their respective backend services. It can also generate API references from your definitions and make them available to your users as API 
documentation.

- API Gateway supports direct integrations that can be configured in the API Gateway user interface (or via the API Gateway’s own API) for the 
following actions:
1. Invoking an AWS Lambda function.
2. Invoking another HTTP endpoint, with or without VPC Link.
3. Making an HTTP call against the API of any AWS service that provides an HTTP API.
4. Returning a mock response generated within API Gateway without calling out to other services.

- Benefits of Amazon API Gateway:
1. Map HTTP requests to specific functions in a Serverless application via an API Gateway event. Connecting HTTP endpoints to individual 
functions is straightforward with API Gateway, obviating the need for a dedicated API server.
2. Map WebSocket events to Serverless functions. If you are building a WebSocket API, API Gateway also lets you map its events to a Serverless 
function. This works great for real-time functionality like in-app updates and notifications.
3. Use multiple microservices to serve the same top-level API. API Gateway makes it easy to have different Serverless functions serving 
different parts of your API. 

- The main use case for Amazon API Gateway is in building serverless HTTP APIs. API Gateway stands in as your API server: managing the schema 
of your HTTP API, connecting each endpoint to the right backend service, and handling the concerns like authentication and throttling.

For more details see [AWS API Gateway Overview](https://www.serverless.com/guides/amazon-api-gateway).

### *AWS API Gateway*
- Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at 
any scale. APIs act as the "front door" for applications to access data, business logic, or functionality from your backend services. Using 
API Gateway, you can create RESTful APIs and WebSocket APIs that enable real-time two-way communication applications. API Gateway supports 
containerized and serverless workloads, as well as web applications.

- API Types :
1. RESTful APIs 
2. WEBSOCKET APIs

- How API Gateway Works

![How API Gateway Works](https://d1.awsstatic.com/serverless/New-API-GW-Diagram.c9fc9835d2a9aa00ef90d0ddc4c6402a2536de0d.png)

- Benefits:
1. Efficient API development.
2. Performance at any scale.
3. Cost savings at scale.
4. Easy monitoring.
5. Flexible security controls.
6. RESTful API options.
 
For more details see [AWS API Gateway](https://aws.amazon.com/api-gateway/).

### *AWS DynamoDB Guide*
- DynamoDB is a hosted NoSQL database offered by Amazon Web Services (AWS). 

- it presents:
1. reliable performance even as it scales;
2. a managed experience, so you won't be SSH-ing into servers to upgrade the crypto libraries;
3. a small, simple API allowing for simple key-value access as well as more advanced query patterns.

- DynamoDB is a particularly good fit for the following use cases:
1. Applications with large amounts of data and strict latency requirements. 
2. Serverless applications using AWS Lambda.
3. Data sets with simple, known access patterns. 

For more details see [AWS DynamoDB Guide](https://www.dynamodbguide.com/what-is-dynamo-db/).

### *AWS DynamoDB*
- How it works:
Amazon DynamoDB is a fully managed, serverless, key-value NoSQL database designed to run high-performance applications at any scale. DynamoDB 
offers built-in security, continuous backups, automated multi-Region replication, in-memory caching, and data export tools.

- Use cases
1. Develop software applications.
2. Create media metadata stores.
3. Deliver seamless retail experiences.
4. Scale gaming platforms.

For mo.re details see [AWS DynamoDB Guide](https://aws.amazon.com/dynamodb/).

### *Dynamoose*
- Dynamoose is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose 
the syntax will be very familar.

- Key Features:
1. Type safety
2. High level API
3. Easy to use syntax
4. Ability to transform data before saving or retrieving documents
5. Strict data modeling (validation, required attributes, and more)
6. Support for DynamoDB Transactions
7. Powerful Conditional/Filtering Support
8. Callback & Promise support

- To install Dynamoose you can run the following command:
      npm install --save dynamoose

- Import
     const dynamoose = require("dynamoose");

For more details see [Dynamoose](https://dynamoosejs.com/getting_started/Introduction/).