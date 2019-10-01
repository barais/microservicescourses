
# Validating complex distributed system: from continuous integration to chaos engineering

----

# Context
- Cloud, virtualisation and virtually infinite resources available
- Versatile consumers with high expectations of
   - Innovative functionalities
   - Quality of services : availability 365/7/24; performance immediate; ...
- Distributed system complexity and scale
- An increasing non-determinism of
   - Hardware precision/bugs/faults and performance
   - Software bugs and performance

----

# THE PROBLEM WITH DISTRIBUTED SYSTEMS

----

## DISTRIBUTED SYSTEMS ARE INHERENTLY CHAOTIC

----

## DISTRIBUTED SYSTEMS ARE INHERENTLY CHAOTIC

- Concretely, what does this mean?

----

### PROBLEM #1

Set of possible system states grows EXPONENTIALLY as sub-component count increases

----

### PROBLEM #2

Failure is **NORMAL** at scale

----
# Cornerstone Test : A zoom on some software Bugs

----
 ### Local bugs

- Some bugs are very local
   - redundant code
   - wrong condition
   - omission
   - lack of checks
   - divide by zero
   - approximations

----

# How to build reliable software ?

----

### Engineering reliable software

- Constructive approach
   - Formal modeling
   - Garantees by construction
- Analytical approach
   - Program analysis
   - Detect and fix and errors
- Fault-tolerance
   - Admit the presence of errors
   - Enhance software with fault-tolerance mechanisms

----

### Constructive approach

- Garantee the absence of bugs
- Top-down approach
- Model-driven development + formal analysis
- Formal proof
   - Automatic or manual
   - Offers exhaustive garantees based on logical modeling and reasoning
   - Examples: Isabelle/HOL, B, KeY, Coq
Used on specific parts of critical software (e.g., certified C compiler)

----

### Constructive approach

- Model checking
   - Formal behavioral model (transition system)
   - Exhaustive verification of properties on model executions (e.g., absence of deadlock, safety and liveness properties)
   - Examples: SCADE, Java PathFinder
   - Used in hardware and software verification
      - at the ‘system’ level for systems engineering (defense, nuclear plant, transportation, etc.)

----

### Analytical approach

- Look for the presence of bugs
- Heuristic-based
- Analyze all sorts of software artefacts (code, models, requirements, etc.)
- Software testing

----

### Fault-tolerance

- Assume that it is impossible to prevent the occurrence of bugs in production software
- Enhance the system with the ability to deal with it
   - Design diversity at the systems level
   - Exception handling at the source code level
   - Randomization at the machine code level

----

### Fault-tolerance

- N-version programming

<div align="center"><img src="resources/bug2.png" width="100%"></div>

----

### Google’s innovation factory

- Google (2012 Update from Larry Page, CEO):
   - Over 850,000 Android devices are activated daily through a network of 55 manufacturers and more than 300 carriers.
   - Google Chrome browser has over 200 million users.
   - Google launched Gmail in 2004 and now is used by more than 350 million people.
   - YouTube has over 800 million monthly users who upload an hour of video per second.

----

### Google’s innovation factory

<div align="center"><img src="resources/bug3.png" width="100%"></div>


----



### DevOps Testing


<div align="center"><img src="resources/devops1.png" width="100%"></div>

----

### DevOps Testing in Dev

<div align="center"><img src="resources/devops2.png" width="100%"></div>

----

### DevOps Testing in Ops

<div align="center"><img src="resources/devops3.png" width="100%"></div>


----

TODO Different kinds àf tests for different kinds of bugs




----

# CHAOS ENGINEERING

- **Systematic** approach to building confidence in the resiliency of distributed systems through triggering chaotic operations

> although that’s FUN, too

----

### CHAOS ENGINEERING

Main idea:

- Inject faults to learn about your system
- Either you find bugs or you build confidence in your system’s behavior

----

### History

- Netflix’s simian army

<div align="center"><img src="resources/chaos1.png" width="40%"></div>

----

### Netflix’s simian army

- Streaming TV network service
   - approx. 40 million subscribers
   - very high dependence on software and cloud (runs on Amazon EC2)
   - major player in open source
- Induce failure regularly
   - ‘break’ production code to check the system’s ability to react
   - Chaos monkey: randomly terminates an instance in production
   - Chaos kong: take an entire region offline
   - Latency monkey: artificial delay in RESTful clients

----

### In this class

- Chaos Engineering but
- Software testing
   - most probably the technique you’ll have to use
- for verification
   - validation is essential but requires the involvement of users => usually done by specific teams, who don’t develop
- from the developer’s perspective
   - you should test your software and you’ll be assigned testing tasks in your future jobs

----

### Chaos Engineering case study

----

TODO Different kinds àf tests for different Microsoft AI feedback
