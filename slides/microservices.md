



### Cloud native application

<div align="center"><img src="resources/diagram-cloud-native.png" width="40%"></div>

<p class="current-visible"
style="position:absolute; left:265px; top:295px;">
<img src="resources/redcircle.svg" width="100%"></p>

Architectural view

----

### Microservices

----

### Modern Software Architecture

- Server Side: Spring Boot, Express, api-platform
- Client Side: Angular, React, Vue
<img src="resources/img8.png" width="100%">

----

### Definition

- A microservices architecture consists of a collection of **small**, **autonomous** services
- Each service is **self-contained** and should implement a **single business capability**

----

### Definition 2

- Microservices is an architectural approach to developing an application as a collection of small services; each service implements business capabilities, runs in its own process and communicates via **HTTP APIs** or **messaging**.

----

<!-- .slide: data-background="./resources/road.png" -->

<h1 style="color:white;"> From a monolithic application</h1>

----

<!-- .slide: data-background="./resources/road1.png" -->

<h1 style="color:white;"> to modular service</h1>


----

### Characteristics of a Microservice

- Services are small, independent, and loosely coupled
- Each service is a separate codebase
- Services can be deployed independently
- Services are responsible for persisting their own data or external state
- Services communicate with each other by using well-defined APIs
- Services don't need to share the same technology stack, libraries, or frameworks

----

### Microservices Overview

<div align="center"><img src="resources/road2.png" width="80%"></div>

----

### Other Components in a Typical Microservices Architecture

- Management
- Service Discovery
- API Gateway

----

### Advantages of Using an API gateway

- It decouples clients from services. Services can be versioned or refactored without needing to update all of the clients
- Services can use messaging protocols that are not web friendly, such as AMQP
- The API Gateway can perform other cross-cutting functions such as authentication, logging, SSL termination, and load balancing

----

### When to use this architecture

- Large applications that require a high release velocity
- Complex applications that need to be highly scalable
- Applications with rich domains or many subdomains
- An organization that consists of small development teams

----

### Benefits

- Independent deployments
- Independent development
- Small, focused teams
- Fault isolation
- Mixed technology stacks
- Granular scaling

----

### Challenges

- Complexity
- Development and test
- Lack of governance
- Network congestion and latency
- Data integrity
- Management
- Versioning
- Skillset

----

### Best Practices

- Model services around the business domain.
- Decentralize everything
- Data storage should be private to the service that owns the data
- Services communicate through well-designed APIs
- Avoid coupling between services
- Offload cross-cutting concerns, such as authentication and - SSL termination, to the gateway or IdP
- Keep domain knowledge out of the gateway
- Services should have loose coupling and high functional cohesion
- Isolate failures

----

### Best Practices

- Model services around the business domain.
- Decentralize everything
- Data storage should be private to the service that owns the data
- Services communicate through **well-designed APIs**
- Avoid coupling between services
- Offload cross-cutting concerns, such as authentication and - SSL termination, to the gateway.
- Keep domain knowledge out of the gateway
- Services should have loose coupling and high functional cohesion
- Isolate failures
