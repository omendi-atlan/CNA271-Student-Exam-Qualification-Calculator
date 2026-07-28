# 2. Monolithic Architecture vs Microservices

This is the heart of the module.

### Monolithic Architecture

In a monolithic system the entire application is built as one single, indivisible unit.

It usually contains:
- The user interface
- The business logic
- The database access

Everything is tightly coupled.  
If one part needs to change or scale, you often have to rebuild and redeploy the whole thing.

**Advantages**
- Simple to start with
- Easy to develop and test in the early stages
- Straightforward deployment (one package)

**Disadvantages**
- Hard to scale specific parts
- Technology lock-in
- A single failure can bring everything down
- Teams step on each other’s toes as the codebase grows

### Microservices Architecture

Microservices take the opposite approach.

The application is broken into small, independent services.  
Each service:
- Does one clear job
- Can be developed, tested, and deployed on its own
- Usually runs in its own container
- Communicates with other services over the network

**Key benefits**
- Scalability – scale only what needs scaling
- Flexibility – different teams can use different technologies
- Agility – smaller, faster releases
- Resilience – if one service fails, the rest can keep running

Our project is not a full microservices system yet.  
It is a single, well-containerized unit.  

But that is exactly how most real microservices journeys begin:  
start with a clean, independent, containerized service, then grow from there.
