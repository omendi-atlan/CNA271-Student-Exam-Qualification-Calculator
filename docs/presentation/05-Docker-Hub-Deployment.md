# 5. Publishing to Docker Hub & Run Instructions

Once the image was built, we pushed it to Docker Hub under the name:

**reneumbra/student-exam-app:latest**

Anyone in the world with Docker installed can now run our application without installing the .NET SDK or even having the source code.

### Exact commands to run it

```bash
docker pull reneumbra/student-exam-app:latest
docker run -it --rm reneumbra/student-exam-app:latest
```

### What the flags mean

- `-it` → interactive terminal (so the user can type marks)
- `--rm` → remove the container automatically when it exits (keeps the machine clean)

### Why this is important

This is the practical demonstration of **portability** and **distribution** — two core cloud-native ideas.

The same image runs on:
- A developer’s laptop
- A lecturer’s machine
- A cloud virtual machine
- A Kubernetes cluster

No “it works on my machine” problems.
