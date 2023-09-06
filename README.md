
![gateway-1024x576](https://github.com/zakizadeh/NewsClient/assets/11499371/3be4df67-6439-4772-9686-7a33c2873856)


# What is the API Gateway pattern?

API, which stands for Application Program Interface, is actually a set of instructions, protocols and tools for building software that will determine how software components interact. API Gateway is a server that acts as a single point of entry. API Gateway can influence the internal architecture of the system and provide an API for each client.


Also, the API Gateway implementation can handle other responsibilities such as authentication, monitoring, load balancing, storage, shaping, request and response management. API Gateway, on the other hand, is responsible for routing the request, combining and translating the protocol, and you should know that all requests sent by the client are made through the API Gateway.


It is after this step that API Gateway can direct the provided requests to the appropriate microservice . As we said, API Gateway can cause the appropriate requests to be routed through it to microservices. You should know that this is possible with the help of one of the following two methods:


 Requests are directed to the appropriate service or proxy.
 
 Requests will be routed or sent to multiple services.
 

# Advantages and disadvantages of implementing API Gateway

As expected, using the API Gateway pattern can have its own advantages and disadvantages. The most important advantage of using an API gateway is that the internal structure of the application will be encapsulated. Therefore, customers can easily interact with this gateway instead of requesting specific services. On the other hand, API Gateway will provide a specific API for each type of client, which will reduce the number of back-and-forth operations between the application and the client.


Other benefits of implementing API Gateway include simplifying programming codes, increasing program efficiency, reducing errors, etc. Of course, API Gateway also has its drawbacks. API Gateway is actually a highly available component that needs to be developed, deployed and managed. On the other hand, there is a risk that the API gateway will also become a development bottleneck. Developers should update the API Gateway to specify endpoints for each microservice.


Therefore, it is very important to make the API Gateway update process as simple and light as possible. Otherwise, developers will be forced to wait in line for API gateway updates. But despite such problems and disadvantages for using API gateways, this model can be introduced as a solution to the problems of applications.


 
# Important points of API Gateway implementation

Now that you have fully familiarized yourself with api gateway and realized the advantages and disadvantages of using it, it is time to point out the various design issues that you should consider when implementing this pattern:


# Performance and scalability:


You should know that today, a handful of companies operate at massive scales that need to handle billions of requests per day. However, for most existing applications, the performance and scalability of the API Gateway is critical. It would be quite natural to implement the api gateway on a platform that supports asynchronous and non-blocking I/O.


Today, there are different types of technology that can be used to implement a scalable api gateway, the most important of which can be mentioned as follows:


 In JVM you can use one of the NIO based frameworks like Netty, Vertx, Spring Reactor or JBoss Undertow.
 
 NGINX Plus
 
 Chrome JavaScript
 
Using the reactive programming model :


API Gateway handles some requests simply by routing them to the appropriate backend service. It can also handle other requests by calling multiple backend services and collecting the results. But some requests are completely independent of each other, and to minimize the response time, the API Gateway pattern must handle independent requests at the same time.


If you write your API Gateway code using a declarative-style reactive method, you can greatly increase the speed of responding to requests. Using the reactive programming model enables you to write very simple yet efficient API Gateway code.


Service call:


A microservice-based application is a distributed system that must use an inter-process communication mechanism. The two styles of interprocess communication are: using a message-based asynchronous mechanism, using a synchronous mechanism. A system typically uses both synchronous and asynchronous process communication styles and can even use multiple implementation styles. To implement API Gateway, it should be noted that this gateway supports different communication mechanisms.


Discover services:


API Gateway needs to know the location (IP address and port) of each microservice it communicates with. In modern cloud-based microservice applications, this point should also be taken into account. Although infrastructure services have a fixed location, determining the service mechanics is not a simple task. Application services have dynamic locations that can change. As a result, api gateway, like any other client in the system, must use the system's service discovery mechanism.


Handling minor failures:


Another issue to consider when implementing an api gateway is the partial failure problem. This issue occurs in all distributed services when a service calls another service that is either slow to respond or unavailable. The api gateway should never wait indefinitely for a downstream service, and during these times, it should handle other requests.


To solve this problem api gateway can return cached data if available. By restoring default data or cached data, the API Gateway implementation ensures that system failures will not affect the user experience.




# Conclusion of api gateway implementation

For most microservice-based applications, it makes sense to implement an api gateway that acts as a single gateway to the system. api gateway is responsible for request routing, composition and protocol translation. This service can provide each client with a custom API and hide problems with back-end services by returning cached or default data. Using the api gateway pattern has its own advantages and disadvantages, but it is still known as a solution to many problems.




NewsClient project covers API discovery with eureka 

to run project : 
1- install Eureka 

2- run NewCms.Endpoints.API
3- run BasicInfo.Endpoints.API
 to create eureka services . 

then : 
4- run NewCMSClient
and go to  localhost/news/index
