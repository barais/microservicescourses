
# Who am I

[Olivier Barais](http://olivier.barais.fr/) , Prof. Univ. Rennes 1, [IRISA DiverSE team]([http](http://www.diverse-team.fr/)

- Validating complex distributed system: from continuous integration to chaos engineering
   - Architecture of a distributed system
   - Introduction to devops
   - Introduction to chaos engineering

<p class="current-visible"
style="position:absolute; right:-100px; top:260px;">
<img src="resources/me.png" width="70%"></p>

---

### Context: HD-Services

- Heterogeneous and Distributed Services
   - Heterogeneous: The infrastructure on which the service runs is composed of a set of different nodes and networks
      - From microcontroller based sensors and devices to cloud.
   - Distributed: The implementation of the services is composed of a set of independent processes communicating asynchronously
      - Truly distributed services implementation is required in order to provide useful and reliable services which take advantage of the infrastructure

----

### Examples

- Health domain and ambient assisted living
- Energy domain and smart grids
- Environmental monitoring and oil and gas
- Safety in hazardous environments
- Intelligent Transport Systems (ITS)
- ...

<img src="resources/context.png" width="70%">

----


### Distributing the implementation

- The service implementation is distributed to exploit the infrastructure

<img src="resources/context1.png" width="70%">


----

### Benefits of HD-Services

- Complex to develop, lots of different skills involved but...
   - Allows fully exploiting the features of each platforms
   - Allow for local and/or decentralized decision making
   - Robust to partial and/or temporary failures
   - Push processing close to data sources
   - Allow for real-time and critical services
   - Can scale in a "big data" context

> In practice for more and  more real-world services are HD-Services

----

### What are the problems?

- Large heterogeneous teams need to collaborate
   - A service architect / developer
   - Many "platform experts"
   - Complex and expensive
   - Unavailable to small actors
- Service maintenance and evolutions
- Infrastructure is dynamic
- Constant evolution/adaptation
- (Early) Validation?
- Software reuse?

> Challenging and expensive

<p class="current-visible"
style="position:absolute; right:-400px; top:260px;">
<img src="resources/context2.png" width="40%"></p>


---

### Cloud(/fog) native application

<div align="center"><img src="resources/diagram-cloud-native.png" width="40%"></div>

----

### Cloud native

<div align="center"><img src="resources/intro.png" width="100%"></div>


----

### Definition

- Cloud-native is an approach to building and running applications that exploits the advantages of the cloud computing delivery model
- Cloud-native is about how applications are created and deployed, not where
- Not related to public or private cloud

----

### Benefit

- When companies build and operate applications in a cloud-native fashion, they bring new ideas to market faster and respond sooner to customer demands

----

### Cloud native application

<div align="center"><img src="resources/diagram-cloud-native.png" width="40%"></div>

----

### Cloud native application

- **Microservices**: Architectural principle of distributed apps
- **Containers**: Shipping, and OS mechanism
- **DEVOPS**: Objectives, team mindset, continuous feedback loop
- **Continuous delivery**: mechanics

<p class="current-visible"
style="position:absolute; right:-420px; top:-150px;">
<img src="resources/diagram-cloud-native.png" width="20%"></p>

----


### Why spending time to understand these concepts


<div align="center"><img src="resources/devops7.png" width="80%"></div>


----


### Talk outline

- Micro-Services
   - API management
- Continuous delivery
   - Continuous integration
   - Continuous deployment
   - Build tool
- DevOps
- Cloud native application validation
   - You mean Bugs ?
   - Verification and Validation using tests
   - Chaos engineering
