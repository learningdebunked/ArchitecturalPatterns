EA 

# ArchitecturalPatterns

- Layered pattern
- Client-server pattern
- Master-slave pattern
- Pipe-filter pattern
- Broker pattern
- Peer-to-peer pattern
- Event-bus pattern
- Model-view-controller pattern
- Blackboard pattern
- Interpreter pattern

Where does hexagonal architecture pattern fit ?

FQDN Vs Header based routing , what are the other types of routing ?
payload compression 

Erlang ( manages its own threads) vs other programming languages ( rely on OS threads ) 

** Architecture frameworks
   ** Zackman framework (knowledge into ontology )
   ** TOGAF
   ** Federal Enterprise architecture framework 
   ** Gartner Enterprise architecture framework

Microservices - come up with a bounded context , self contained components

A good architect starts with customer , watch your customer work with our software

Design patterns - Building blocks of architecture

Read code
Understand any open source project 
O'reilly architecture conference

Conway's Law:  communication structure and architecture have to match

BUFD - Big upfront Design , leans on water fall model

Technology decision is deferred last responsible moment in Agile incremental designs i.e. building around users

DDD ( domain driven design )  - structure of code maps to structure of problem domain/ business , in fact it must match otherwise its leads to conway mismatch 

Bounded context - // TODO how can this be modelled in real code 

What is a user story ?
- Describes an end user going through a domain level process to achieve valuable outcome
- story should fit on a single sticky note
- don't get into horizontal slicing like UI / Business and data logic ( this happens at Walmart ) , instead do Vertical slicing , make it smaller by narrowing its scope
- Activity diagram might be a good start to vertical slice
- apply work flow isolation , narrow the scope and this is the most common one

Bounded context 
- Event storming in the DDD  , this is the first step , domain level events that are meaningful to the business , business usually drive this process
- Domain gives coherence to the architecture from event storming
- what is an agent and how to implement ? //TODO
- Entities are the bounded context in agents, where an agent does contextual work linked to a respective event and action. //Understand more in detail

An enterprise-level agile system is comprised of small, cooperating but stand-alone parts, whereas EA is one large system.

**Characteristics of DDD**

    ** Structure of code should map to domain , the problem that is solved
    **  DDD is incremental , no Big upfront Design , i.e. inspect & adapt & improve
    **  Microservice is the common way DDD is implemented
    ** Domain driven design is organizing code along certain well defined boundaries
    ** Bounded context -- Natural division within a business , things that go inside the context happen within the context 
    ** Entity -- individual within a given context . Much like an object or a class in a object oriented world. Has one job and does one thing with a specific context
    ** Aggregate -- collection of entities that you talk to through a single portal 
    ** Line b/w Entity and Aggregate can be fuzzy. 
    ** Determining whether its an Entity or Aggregate may not be visible from outside the context 
    ** Portal entity uses other entities within aggregates to accomplish tasks
    ** Context can be implemented by single aggregate or multiple aggregates
    ** Ubiquituous language 

          ** People working within an context use a language all their own
          ** Language of one context is different from language of other contexts
          ** Formalizing this language is essential for DDD , within a specific context
          ** Identifies roles for entities and entities are named after roles
          ** 

    ** Everything is context sensitive inside DDD
    ** How entities communicate ?

          ** Easy  : Orchestrate Declarative systems , one entity tells other what to do  , exmaple shopping service telling invoice service to issue billing , notification to send out emails

                  ** Leads to tight coupling b/w services
                  ** 
                  
          ** Better: Choreography or reactive systems

                  ** Replace the services with generic ones , example shopping service now announces to the world like order place() event , so notification picks it , billing picks it
                  ** Eliminates hard tight coupling
                  ** Maintainence is easy
                  ** Reactive model is way to go for DDD
                  ** How do we design ?

                           ** Event storming : 
                           
                                 ** Used it to analyse the domain and develope the code
                                 ** Model Flow of activities within business
                                 ** Tools for event storming :  1 event per sticky note 
                           
                  

Architectural patterns 
- Monolith - every thing happens in one big program. Cost of replacing a monolith is lower than maintaining . A well structured monolith has horizontal and vertical partitions
  Horizontal partitions are called Tiers ( like UI / Business logic and / Database ) .
    - Tiers talk to immediate neighbors typically UI never talks to DB
    - Vertical partitions - Reflect the bounded context of the domain
      
- Plugin or the micro kernel pattern
   - Example : OS
   - Single standalone executable
   - Kernel handles virtual memory or file system , others are plugged into the kernel
   - Linux is another example , every thing else is plugged into Kernel
   - //TODO see a real life example and implementation
   - The communication is mostly via message bus or a http REST Interface
   - Amazons AWS / Microsoft Azure are one example of Micro kernel pattern
   - Plugins don't know how other plugins work or even exist

  - Message based architecture
     - Takes micro kernel pattern a step further
     - Message bus controls the flow of communication
     - Adaptors talk to the applications
     - Programs talk over message bus through messages
     - Pub/sub model , instead of queue , agents subscribe to the broker

  - Micro services
     - A cloud of small independent services that come together to get larger work done
     - Have to be fully autonomous
     - should implement bounded contexts
     - come up with a design and run time complexity

 - Reactive or choreographed pattern
     - Declarative approach is a maintainence headache
     - Relies on events , instead of making requests
     -             

 Layered Architecture: Separates concerns into hierarchical layers like presentation, business logic, and data access. This is a tried and true way to structure applications.

- Event-Driven Architecture: Has become popular for highly scalable apps. Components publish and react to events from other components asynchronously.

- Microkernel Architecture: Minimizes shared core software and implements other functionality in external modules. This provides flexibility.

- Space-Based/Actor Model Architecture: Implements objects/actors that communicate via asynchronous messaging. This is ideal for concurrent distributed systems.

In 2024, architectural trends focus on scaling, resilience, and flexibility:

- Serverless Architectures: Using cloud services like AWS Lambda, these architectures scale automatically without provisioning servers.

- Mesh App Architectures: Build on a distributed data layer so features can be added without monolithic rewrites.

- Event Streaming and Complex Event Processing (CEP) Integration: Enables real-time response to diverse events.

- Reactive Principles and Non-Blocking Communication: Facilitates resilience and elasticity.
- 
![image](https://github.com/learningdebunked/ArchitecturalPatterns/assets/7702406/2dd37368-b933-4bba-9e1d-bfd2906c3a70)

![image](https://github.com/learningdebunked/ArchitecturalPatterns/assets/7702406/c981ebb1-2d33-4fcc-90da-8082c96e1006)


![image](https://github.com/learningdebunked/ArchitecturalPatterns/assets/7702406/f1000294-2878-42a9-9ca8-d90c6f5f68af)

