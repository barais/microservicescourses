
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

 ### Integration bugs

- Some bugs happen when integrating components/services
   - incompatibilities between library dependencies
   - unspecified contract
   - ...


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

### Unit Testing
   - Test each unit individually to make sure it works properly on its own.
   - Can be performed at any time.
   - Can only detect errors within a single unit.

----

### Integration Testing

- Test units together to make sure they can be incorporated with each other without issue.
- Is performed after unit testing.
- Can detect errors resulting from units interacting with one another.

----

### System testing

- Ensure the correct behavior of the complete system
- Automated visual UI testing
- selenium (https://www.seleniumhq.org/selenium-ide/)

----

### Load testing

- test performance both on static and dynamic resources
- jmeter (https://jmeter.apache.org/)

----

### Pen testing

- Penetration testing.
- Metasploit, a framework to build custom tools for specific tasks. (https://www.metasploit.com/)

----

# Problem with testing

How to qualify the quality of tests

----

### Test Your Tests

- What do you expect from test cases?
   - Cover requirements
   - Code coverage
   - Stress the application
   - **Reveal bugs**


----

### Example

<div align="center"><img src="resources/chaos20.png" width="100%"></div>


----

### Example

<div align="center"><img src="resources/chaos21.png" width="100%"></div>

----

### Mutation testing

<div align="center"><img src="resources/chaos22.png" width="100%"></div>

----

### Limitations of mutation testing

- Expensive computation
- Huge number of mutants
- Presence of equivalent mutants
   - => Extreme Mutation

----


### Extreme Mutation testing

- Proposed in 2016 by Niedermayr et al.
- Remove the body of the method
- Replace by a single return
- Less mutants
- Most equivalent mutants can be detected



----

### Example

<div align="center"><img src="resources/chaos26.png" width="100%"></div>

----

### Example

<div align="center"><img src="resources/chaos25.png" width="200%"></div>


----

### But ...

- You are doing enough testing if the following is true:
   - YOU RARELY GET BUGS THAT ESCAPE INTO PRODUCTION
    - YOU ARE RARELY HESITANT TO CHANGE SOME CODE FOR FEAR IT WILL CAUSE PRODUCTION BUGS
> Martin Fowler


----

### PROBLEM 1

Systems states to test had grown **EXPONENTIALLY**

and you could not attempt (and you will fail) to scale your testing effort EXPONENTIALLY


----

### CONFIDENCE IN SYSTEM HEALTH


- Testing explores the n dimensional space described by the set of all possible system states and operations

<div align="center"><img src="resources/chaos5.png" width="40%"></div>

----

### CONFIDENCE IN SYSTEM HEALTH


- Testing explores the n dimensional space described by the set of all possible system states and operations

<div align="center"><img src="resources/chaos6.png" width="40%"></div>

----

### CONFIDENCE IN SYSTEM HEALTH


- Testing explores the n dimensional space described by the set of all possible system states and operations

<div align="center"><img src="resources/chaos7.png" width="40%"></div>

----

### CONFIDENCE IN SYSTEM HEALTH


- Testing explores the n dimensional space described by the set of all possible system states and operations

<div align="center"><img src="resources/chaos8.png" width="40%"></div>


----

### CONFIDENCE IN SYSTEM HEALTH

- As system complexity increases, the states and operations that must potentially be tested increase exponentially
- Curse of dimensionality

<div align="center"><img src="resources/chaos9.png" width="40%"></div>


----

# TOO MANY system states to test

- And correctly reducing the test set is too expensive

----

# WE STILL WANT CONFIDENCE IN SYSTEM RELIABILITY


----

### RANDOMNESS

- Reduces test set in an evenly distributed way that avoids engineer bias and blind spots

- Generating test cases is very CHEAP, enabling more tests to be run

<div align="center"><img src="resources/chaos10.png" width="30%"></div>


----

## MONTE CARLO APPROACH TO SYSTEM CONFIDENCE

<div align="center"><img src="resources/chaos11.png" width="100%"></div>


----
### TELEMETRY is essential

- WITHOUT IT, YOU’RE NOT LEARNING ANYTHING ABOUT YOUR SYSTEM

<div align="center"><img src="resources/chaos12.png" width="50%"></div>


----

### CASE STUDY : FAILURE IS INEVITABLE AT SCALE

- LEARNING LESSONS THE HARD WAY
   - THE 2 AM PHONE CALL ( Microsoft Azure Search)

----

### CASE STUDY : FAILURE IS INEVITABLE AT SCALE

- LEARNING LESSONS THE HARD WAY
    - Secondary failures caused by a bug in ERROR RECOVERY LOGIC

----


### CASE STUDY : FAILURE IS INEVITABLE AT SCALE

- LEARNING LESSONS THE HARD WAY
    - Resulted in multiple engineers fixing clusters by hand ALL NIGHT (including the boss ;)


----

### WHAT HAPPENED!?

- Code is widely tested but ...
- HOW CAN YOU TRUST ERROR RECOVERY CODE IF IT NEVER RUNS?


----

<div align="center"><img src="resources/chaos13.png" width="70%"></div>


----

<div align="center"><img src="resources/chaos14.png" width="70%"></div>


----

<div align="center"><img src="resources/chaos15.png" width="70%"></div>


----


### Problem 2

- Failure is **INEVITABLE** at scale
- But not **DETERMINISTICALLY**
   - And not reliably within a sprint cycle



----

# Promote FAILURE to a FIRST-CLASS member of the system

----

### AUTOMATED, RANDOM, CONTINUOUS TESTS

<div align="center"><img src="resources/chaos16.png" width="70%"></div>


----
### SEARCH CHAOS MONKEY

<div>
<ul>
<li>
Trigger random faults regularly
</li>

<ul>
<li>
Restart VMs
</li>
<li>
Restart processes
</li>
<li>
Simulate network connection loss
</li>
<li>
Crash VMs
</li>
</ul>

</div>
<!-- .element: class="left" -->

<div>
<div align="center"><img src="resources/chaos17.png" width="90%"></div>

</div>
<!-- .element: class="right" -->




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

# SUMMARY

----

### SUMMARY



- DISTRIBUTED SYSTEMS ARE CHAOTIC AND REQUIRE CHAOTIC TESTING METHODS
- MONTE CARLO-STYLE RANDOM SAMPLING IS A CHEAP WAY TO GAIN CONFIDENCE ABOUT SYSTEM HEALTH
- ... AS LONG AS YOU INCLUDE FAILURE IN YOUR SAMPLE SET


----

### AFTER CHAOS ENGINEERING

HIGH CONFIDENCE IN SYSTEM QUALITY (Microsoft Azure Search)

<div align="center"><img src="resources/chaos18.png" width="80%"></div>


----

### In this class

- Chaos Engineering but
- Software testing
   - most probably the technique you’ll have to use
- For verification
   - validation is essential but requires the involvement of users => usually done by specific teams, who don’t develop
- From the developer’s perspective
   - you should test your software and you’ll be assigned testing tasks in your future jobs
