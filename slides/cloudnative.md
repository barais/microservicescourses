# Cloud native

----
### Cloud Native Container Design Principles

<div align="center"><img src="resources/cloudnative.png" width="100%"></div>

----

### Build time:

- Single Concern: Each container addresses a single concern and does it well
- Self-Containment: A container relies only on the presence of the Linux kernel. Additional libraries are added when the container is built
- Image Immutability: Containerized applications are meant to be immutable, and once built are not expected to change between different environments

----

### Runtime:

- High Observability: Every container must implement all necessary APIs to help the platform observe and manage the application in the best way possible
- Lifecycle Conformance: A container must have a way to read events coming from the platform and conform by reacting to those events
- Process Disposability: Containerized applications must be as ephemeral as possible and ready to be replaced by another container instance at any point in time
- Runtime Confinement: Every container must declare its resource requirements and restrict resource use to the requirements indicated


----

# Monitoring tools

- [https://www.monperrus.net/martin/monitoring.pdf](https://www.monperrus.net/martin/monitoring.pdf)

