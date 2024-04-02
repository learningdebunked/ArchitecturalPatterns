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
   ** Zackman framework
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
- Event storming in the DDD 
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
