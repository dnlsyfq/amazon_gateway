# AWS Gateway
API Gateway is a managed service provided by AWS that makes creating, deploying and maintaining APIs easy. API Gateway includes features to:

* Transform the body and headers of incoming API requests to match backend systems
* Transform the body and headers of the outgoing API responses to match API requirements
* Control API access via AWS Identity and Access Management
* Create and apply API keys for third-party development
* Enable Amazon CloudWatch integration for API monitoring
* Cache API responses via Amazon CloudFront for faster response times
* Deploy an API to multiple stages, allowing easy differentiation between development, test, production as well as versioning
* Connect custom domains to an API
* Define models to help standardize your API request and response transformations










## Couple Amazon API Gateway and AWS Lambda
A microservice using Amazon API Gateway consists of a defined resource and associated methods (GET,POST,PUT,etc) in API Gateway
as well as the backend target.

### Using an Amazon API Gateway endpoints that invokes an AWS Lambda function.

Backend target will be lambda function or another HTTP endpoint ( 3rd party API or listerning web server), an AWS service proxy
or a mock integration to be used as a placeholder.

### Amazon API Gateway and AWS Lambda Terminology

* **Resource**: Represented as a URL endpoint and path. For example, . You can associate HTTP methods with resources and define different backend targets for each method. In a microservices architecture, a resource would represent a single microservice within your system.

* **Method**: In API Gateway, a method is identified by the combination of a resource path and an HTTP verb, such as GET, POST, and DELETE.

* **Method Request:**  The method request settings in API Gateway store the methods authorization settings and define the URL Query String parameters and HTTP Request Headers that are received from the client.

* **Integration Request:** The integration request settings define the backend target used with the method. It is also where you can define mapping templates, to transform the incoming request to match what the backend target is expecting.

* **Integration Response:**  The integration response settings is where the mappings are defined between the response from the backend target and the method response in API Gateway. You can also transform the data that is returned from your backend target to fit what your end users and applications are expecting.

* **Method Response:** The method response settings define the method response types, their headers and content types.

* **Model:** In API Gateway, a model defines the format, also known as the schema or shape, of some data. You create and use models to make it easier to create mapping templates. Because API Gateway is designed to work primarily with JavaScript Object Notation (JSON)-formatted data, API Gateway uses JSON Schema to define the expected schema of the data.

* **Stage:** In API Gateway, a stage defines the path through which an API deployment is accessible. This is commonly used to deviate between versions, as well as development vs production endpoints, etc.

* **Blueprint:** A Lambda blueprint is an example lambda function that can be used as a base to build out new Lambda functions.


