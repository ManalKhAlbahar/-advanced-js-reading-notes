# Read17 :  AWS: S3 and Lambda
* AWS S3.
* AWS Lambda Basics.
* AWS Lambda Functions.
* CDN.

### *AWS S3*
- Amazon Simple Storage Service (Amazon S3) is an object storage service offering industry-leading scalability, data availability, security, and 
performance. Customers of all sizes and industries can store and protect any amount of data for virtually any use case, such as data lakes, 
cloud-native applications, and mobile apps. With cost-effective storage classes and easy-to-use management features, you can optimize costs, 
organize data, and configure fine-tuned access controls to meet specific business, organizational, and compliance requirements.

- Use cases:
1. Build a data lake.
2. Back up and restore critical data.
3. Archive data at the lowest cost.
4. Run cloud-native applications.

For more details see [AWS S3](https://aws.amazon.com/s3/).

### *AWS Lambda Basics*
- AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS). Users of AWS Lambda create functions, self-contained 
applications written in one of the supported languages and runtimes, and upload them to AWS Lambda, which executes those functions in an efficient 
and flexible manner.

- The Lambda functions can perform any kind of computing task, from serving web pages and processing streams of data to calling APIs and 
integrating with other AWS services.

- The concept of “serverless” computing refers to not needing to maintain your own servers to run these functions. AWS Lambda is a fully managed 
service that takes care of all the infrastructure for you. And so “serverless” doesn’t mean that there are no servers involved: it just means that 
the servers, the operating systems, the network layer and the rest of the infrastructure have already been taken care of, so that you can focus on 
writing application code.

- When building Serverless applications, AWS Lambda is one of the main candidates for running the application code. Typically, to complete a 
Serverless stack you’ll need: a computing service; a database service; and an HTTP gateway service.

- Due to Lambda’s architecture, it can deliver great benefits over traditional cloud computing setups for applications where:
individual tasks run for a short time; each task is generally self-contained; and there is a large difference between the lowest and highest 
levels in the workload of the application.

- Limitations of AWS Lambda:
1. Cold start time
2. Function limits
3. Not always cost-effective
4. Limited number of supported runtimes

For more details see [AWS Lambda Basics](https://www.serverless.com/aws-lambda).

### *AWS Lambda Functions*
- How it works?
AWS Lambda is a serverless, event-driven compute service that lets you run code for virtually any type of application or backend service without 
provisioning or managing servers. You can trigger Lambda from over 200 AWS services and software as a service (SaaS) applications, and only pay 
for what you use.

- Use cases
1. Process data at scale
2. Run interactive web and mobile backends
3. Enable powerful ML insights
4. Create event-driven applications

For more details see [AWS Lambda Functions](https://aws.amazon.com/lambda/).

### *CDN*
- Content Delivery Network (CDN) is a geographically distributed group of servers that work together to provide fast delivery of Internet content. 
A CDN allows for the fast transfer of data needed for loading Internet content including HTML pages, javascript files, stylesheets, images, and 
videos.

- CDNs work through servers nearest to the website visitor respond to the request. The content delivery network copies the pages of a website to a 
network of servers that are spread out at geographically different locations, caching the contents of the page. When a user requests a webpage 
that is part of a content delivery network, the CDN will redirect the request from the originating site’s server to a server in the CDN that is 
closest to the user and deliver the cached content. CDNs will also communicate with the originating server to deliver any content that has not 
been previously cached. In turn, the speed is improved by distributing content closer to the website visitors by using a nearby CDN server, 
causing visitors to experience faster page loading times. In simpler terms, for example, instead of a user in London trying to access a server in 
LA, which can cause slower Internet speeds, the user would be redirected through a CDN that is geographically closest to them (London, Paris, 
Stockholm, etc). As of today, the majority of web traffic goes through through CDNs, including traffic from major sites like Facebook, Netflix, 
and Amazon.


For more details see [CDN](https://cyberhoot.com/cybrary/content-delivery-network-cdn/).