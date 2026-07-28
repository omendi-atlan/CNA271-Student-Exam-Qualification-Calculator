# 7. Cloud Native Concepts Demonstrated

Even though this is a small project, it already applies several important cloud-native principles.

### 1. Containerization
The application and its runtime are packaged together into a single portable unit.

### 2. Immutability
Once the image is built, it does not change.  
Every run of the same tag produces the same behaviour.

### 3. Portability
The image runs the same way on any machine that has Docker — Windows, Linux, or cloud.

### 4. Declarative configuration
The Dockerfile describes the desired end state.  
We do not write long imperative scripts; we declare what we want.

### 5. Distribution via a registry
By pushing to Docker Hub we made the application discoverable and runnable by anyone.

### 6. Independence
This calculator can later become one microservice in a larger system.  
Other services (for example a student portal or a results service) could call it without caring how it is implemented internally.

### Looking ahead
In a full microservices architecture we might later:
- Add an API layer in front of this logic
- Deploy multiple instances behind a load balancer
- Orchestrate it with Kubernetes
- Add monitoring and health checks

We have already laid the correct foundation.
