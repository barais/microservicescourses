# Continuous delivery

----

### Continuous delivery

<div align="center"><img src="resources/diagram-cloud-native.png" width="40%"></div>

<p class="current-visible"
style="position:absolute; left:492px; top:58px;">
<img src="resources/redcircle.svg" width="100%"></p>

----
Outline

- What?
- Why?
- How?

----


### What’s Continuous Delivery?

- **Continuous Integration (CI)**
   - The process of constantly merging development with a master branch for testing (as in on a daily basis)
- **Continuous Delivery (CD)**
   - The practice of automatically deploying code to internal systems for further testing as soon as committed changes have passed automated tests

----

### Other Definition

- *Continuous Integration is a software development practice where members of a team integrate their work frequently, usually each person integrates at least daily - leading to multiple integrations per day. Each integration is verified by an automated build (including test) to detect integration errors as quickly as possible.*

http://martinfowler.com/articles/continuousIntegration.html


----
### What is Continuous Integration?

The **practice** of **integrating** source code **continuously**

----


<video controls width="100%">
    <source src="resources/ci.mp4"
            type="video/mp4">
    Sorry, your browser doesn't support embedded videos.
</video>

----


### What is “integration” ?

At a minimum:
- Gather latest source together
- Compile
- Execute tests
- Verify success

----

### What is “integration” ?

Can include other tasks such as:
- Rebuild the database
- Build release distribution
- Run code analysis and coverage tools
- Generate documentation

----

### How often is continuously?

- As frequently as possible
- More like once per hour than once per day
- Before leaving at the end of the day

----

### When to integrate?

- Implement just enough, then integrate
- If using Test Driven Development, it forms a natural break in the cycle
- Taking small steps

<div align="center"><img src="resources/ci.png" width="70%"></div>

----

# Why?

<div align="center"><img src="resources/ci2.png" width="70%"></div>


----

### Why?

<p align="left">Regular feedback:</p>
- For the integrator : “Did that work?”
- For the rest of the team : “Is the build OK?”
- Reduces Risk overall

----

### Why?

<p align="left">Reduce integration pain</p>

- No more ‘*merge hell*’
- XP Mantra: Do the ‘*hard things*’ often so they’re not hard any more

----
### Why?

<p align="left">Increased automation</p>

- Don’t repeat yourself - automate to increase speed and to make less mistakes

----

# How?

----

### Technical pre-requisites

- Source Code checked into Source Control
- Automated (fast) build
   - Compile
   - Test
   - Command line without interaction
- Dedicated (communal) Integration Machine

----
### Technical pre-requisites

<div align="center"><img src="resources/ci5.png" width="70%"></div>

----

### Social pre-requisites

- Developer discipline
   - Continuous means continuous, not 'once per week'
- Shared ownership

----

### Automated CI

<p align="left">Automated Continuous Integration Server</p>

- CruiseControl, CruiseControl.NET, TeamCity, Bamboo, etc.
- Detects changes in source control
- Launches integration build
- Publishes results

----

### Why use Automated CI?

- Makes integration easy
- Guarantees integration happens
- Better feedback options
- Encourages test automation
   - Through metrics

----
### Immediate Feedback is Key

<div align="center"><img src="resources/ci1.png" width="90%"></div>

----

### Build manager

A build tool + A dependency management tool


- maven, graddle ivy
- npm, grunt, gulp
- composer
- ....

----

### Objectives

- Make the development process visible or transparent
- Provide an easy way to see the health and status of a project
- Decreasing training time for new developers
- Bringing together the tools required in a uniform way
- Preventing inconsistent setups
- Providing a standard development infrastructure across projects
- Focus energy on writing applications

----

### Benefits

- Standardization
- Fast and easy to set up a powerful build process
- Dependency management (automatic downloads)
- Repository management
- Extensible architecture

----


# Show me!

----

### Continuous deployment: the Basic Idea

- Commit frequently to reduce merge issues
- Automatically test each commit
- Automatically create a production candidate build for each successfully tested commit
- Deploy that build to necessary environments for manual testing
- Deploy builds that pass manual testing to production

----

### Continuous Deployment

- The practice of automatically deploying code to production as soon as committed changes have passed automated tests
- Basically removing manual testing from the picture
- Automated tests have to be fantastic
- Not for every situation, especially as bigger organizations usually need approvals in order to deploy
