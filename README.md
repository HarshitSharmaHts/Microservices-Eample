# MicroServices Example

## What are Micrioservices?

According to [microservice.io](https://microservices.io/): 
Microservices - also known as the microservice architecture - is an architectural style that structures an application as a collection of loosely coupled services, which implement business capabilities. The microservice architecture enables the continuous delivery/deployment of large, complex applications. It also enables an organization to evolve its technology stack.

## Microservice Architecture

<img src="https://cdn.nginx.com/wp-content/uploads/2015/06/Graph-09.png"
     alt="API Gateway"
     style="margin:10px;border-radius:5px;width:100%;"/>

In microservices architecture we broke down our application into task level services. And all the client interaction happens to the exposed API Gateway, which controls the routing on REST calls to an appropriate REST Service.

For example:
We have two services `Student Service` and `Teacher Service` and both the services are running on port number 8081 and 8082 respectively. so for client only the port number 8080 will be exposed where the API Gateway is running.

And API Gateway is responsible for serving the data on the behalf of other services;

see below request mapping:

localhost:8080/students will be mapped to localhost:8081

		and

localhost:8080/teachers will be mapped to localhost:8082

## About the project

In the above project there are three sprin-boot-project
```
1. API Gateway (This API was created using the Netflix Zuul)
2. Student Service (REST API)
3. Teacher Service (REST API)
```

setup these three spring boot project in your sts suite and run them all.
