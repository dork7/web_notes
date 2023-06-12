Design Patterns

- [ ] 		Service Registry
- [ ] 		Circuit Breaker
- [ ] 		API Gateway
- [ ] 		Event-Driven Architecture
- [ ] 		Database per Service
- [ ] 		Command Query Responsibility Segregation (CQRS)
- [ ] 		Externalized Configuration
- [ ] 		Saga Pattern
- [ ] 		Bulkhead Pattern
- [ ] 		Backends for Frontends (BFF)



# Microservice architecture

`Breaking a big application into small, simple and independent modules/applications.`

## PROS
- Easy to manage
- Scalable 
- Easy to deploy
- Technology independent
- Decoupled
- Easy CI/CD
- Easy to understand
- single point of failure

## CONS
- inter process communication
- a lot of error handling
- debugging issues
- distributed transactions
- More resource utilization
- Data duplication


# Design Patterns

# API Gateway
Suppose you have to get product details, shipping details, reviews, billing information for a certain product, in that case you'll have to call 3 to 4 microservices from the client side to get all the required information. Which will be expensive. So to overcome this API gateway pattern can be used.

API gateway is responsible for getting the data from multiple microservices, combine the data then send it to client,

In this case only one endpoint is exposed to the client, and client will be making only one external call. API gateway service will be responsible to gather all the data from different MS, and return data. 

As api gateway and other services are on same network, so it will be fast asf. API gateway can also make parallel calls.

We can also have multiple api gateways, for example for mobile, webapp, third party etc.


## Pros
- Authentication
- SSL termination ( HTTPS can be verified at api gateway, rest of the calls can happen without HTTPS)
- Load Balancer
- Insulation
- Translation ( rest to soap )
- Caching
- managing access

## Cons
- Increase in hops
- Complicated


# Service discovery
<!-- Let's say client wants to communicate to the service directly, and one microservice is running multiple instances,  -->
API gateway/load balancer needs to know what is the IP address of the service that it wants to communicate? that's where the concept of service discovery comes in.

Service register DB is the service which contain all the information of the instances, i.e instance name, ip address.

## Self Registry:
    When a service container comes up,it will register itself, in the registry service. Every X number of time, the services will update their address in the SR microservice.

## Third party:
    SR service will be listening to the events in cluster, whenever their is update in cluster, it will get the address of that service. 

Service registry can also talk to load balancer to increase the instances.


