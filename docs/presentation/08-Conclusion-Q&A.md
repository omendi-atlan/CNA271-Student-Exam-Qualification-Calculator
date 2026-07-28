# 8. Conclusion & Q&A

### What we delivered

- A working C# console application with correct weighted calculation and validation
- A multi-stage Dockerfile following current best practices
- A publicly available image on Docker Hub
- Clear documentation so anyone can run the application with two Docker commands
- A structured presentation that links the practical work back to the theory of the module

### Key takeaways

1. Containerization turns even a simple program into a portable, independent unit.
2. Multi-stage builds keep production images small and secure.
3. Publishing to a registry removes the “works on my machine” problem.
4. This is the natural first step toward a microservices architecture.

### Lessons learned

- Writing a good Dockerfile is as important as writing the application code.
- Documentation is not optional — it is part of the product.
- Working as a group forces us to communicate clearly and divide responsibility.

### Thank you

We are happy to take any questions.

---

**Possible questions and short answers (see Speaker-Notes.md for fuller versions)**

- Why multi-stage builds?  
  Smaller, safer final images.

- Why not a full microservices system?  
  The brief asked for a single containerized application as the starting point.

- Can this run on Kubernetes?  
  Yes. The same image can be deployed as a Deployment or Job.
