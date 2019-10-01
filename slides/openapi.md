# well-designed APIs

----

### API

- API: interface or communication protocol between a client and a server intended to simplify the building of client-side software
- It is a “**contract**” between the client and the server, such that if the client makes a request in a specific format, it will always get a response in a specific format or initiate a defined action

----

### Web API

A server-side web API is a programmatic interface consisting of one or more publicly exposed endpoints to a defined request–response message system, typically expressed in JSON or XML, which is exposed via the web—most commonly by means of an HTTP-based web server

----

### OpenAPI

- The OpenAPI Specification (OAS) defines a standard,
programming language-agnostic interface description
for Web APIs, which allows both humans and
computers to discover and understand the capabilities
of a service

----

### Why openAPI

- Use cases for machine-readable API definition
documents include, but are not limited to:
   - interactive documentation
   - code generation for documentation,
   - code generation for clients, and servers
   - automation of test cases

----

### Application Programming Interface description language

```js
{
  "swagger": "2.0",
  "info": {
    "description": "This is a sample server Petstore server.",
    "version": "1.0.0",
    "title": "Swagger Petstore",
    "termsOfService": "http://swagger.io/terms/",
    "contact": {
      "email": "apiteam@swagger.io"
    },
    "license": {
    "name": "Apache 2.0",
    "url": "http://www.apache.org/licenses/LICENSE-2.0.html"
  }
},
```

----

### Interactive documentation

<p class="current-visible"
style="position:absolute; left:0; top:100;">
<img src="resources/openapi0.png" width="100%"></p>

----

### Linter


<div>


Open Source Linting Engine
- Based on https://speccy.io
- https://github.com/stoplightio/spectral
</div>
<!-- .element: class="left" -->

<div>
<p class="current-visible"
style="position:absolute; left:550px; top:-20px;">
<img src="resources/openapi3.png" width="650px">
<img src="resources/openapi2.png" width="150%" style="position:absolute; left:100px; top:200px;"></p>

</div>
<!-- .element: class="right" -->

----

### Mocker


<div>
Prism 3
- Open Source Mock Server
- Complete rewrite in TypeScript

<p class="current-visible"
style="position:absolute; left:0px; top:300px;">
https://github.com/stoplightio/prism
</p>
</div>
<!-- .element: class="left" -->

<div>
<p class="current-visible"
style="position:absolute; left:500px; top:30px;">
<img src="resources/openapi4.png" width="650px">
<img src="resources/openapi5.png" width="150%" style="position:absolute; left:100px; top:200px;"></p>

</div>
<!-- .element: class="right" -->

----

### OpenAPI and API gateway
<p align="left">API Gateway: a server that acts as an API front-end, receives API requests, enforces throttling and security policies, passes requests to the back-end service and then passes the response back to the requester. Often support:</p>

- analytics
- caching
- authentication
- authorization
- security
- audit
- regulatory compliance.
- monetization: functionality to support charging for access to commercial APIs.

----

### OpenAPI compatible with the main

- Compatible with the main players
   - AWS API Gateway
   - Apigee Edge
   - Microsoft API Management
   - tyk.io (opensource)

----

### The rules (to make it happen)

<p align="left">Use an API Gateway</p>
- Put as much as you can on it (security, rate limiting, payload validation)
- You do not need micro services to use an API Gateway
- Make sure what exposes matches what’s declared in the OpenAPI spec file
- Prefer a solution that is declarative
- It’s going to be easier to write automation scripts
- Refrain from using custom extension
- It will complicate the things the day these automations will be the standard for all the solutions
