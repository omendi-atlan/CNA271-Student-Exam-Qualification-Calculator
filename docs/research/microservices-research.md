# Research Notes – Monolithic vs Microservices

## Monolithic Architecture

A monolithic application is built as a single deployable unit.  
All features share the same codebase, the same process, and usually the same database.

**Typical characteristics**
- One large codebase
- Shared memory and data access
- Single deployment package
- Scaling means scaling the entire application

**When it works well**
- Small teams
- Simple domains
- Early stages of a product

**Common problems as the system grows**
- Long build and test times
- Difficulty adopting new technologies
- Risk of cascading failures
- Coordination overhead between developers

## Microservices Architecture

Microservices structure an application as a collection of loosely coupled services.  
Each service owns its own data and can be developed, deployed, and scaled independently.

**Typical characteristics**
- Small, focused services
- Independent deployment
- Communication over the network (usually HTTP/REST or messaging)
- Often containerized and orchestrated

**Main benefits**
- Independent scaling
- Technology diversity
- Faster, smaller releases
- Better fault isolation
- Alignment with team boundaries (Conway’s Law)

**Trade-offs**
- Increased operational complexity
- Network latency and partial failure handling
- Distributed data consistency challenges
- Need for good observability and automation

## How our project fits

We built one independent, containerized service.  
It has a clear responsibility (calculate exam qualification), a well-defined interface (console input/output), and is distributed through a registry.

This matches the recommended starting point for moving toward microservices:  
create clean, independently deployable units first, then compose them later.

## Key references for further reading

- Martin Fowler – Microservices
- Sam Newman – Building Microservices
- Microsoft .NET container documentation
- Docker multi-stage builds best practices
