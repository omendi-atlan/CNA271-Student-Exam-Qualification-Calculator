# Full Speaker Notes – CNA271 Presentation

These notes are written in natural spoken language so every group member can sound confident and human.  
Read them a few times before presentation day. Adjust the wording slightly to match your own voice.

---

## Member 1 – Opening & Agenda (≈ 60 seconds)

“Good morning everyone.  
We are the group presenting the Student Exam Qualification Calculator for CNA271.

Today we will walk you through how we built a simple console application, containerized it properly, published it to Docker Hub, and how it connects to the bigger ideas of microservices and cloud-native development.

Here is our agenda…”  
*(show or read the agenda quickly)*

“Every member of the group will speak, and we will all take part in the live demonstration.”

---

## Member 2 – Monolithic vs Microservices (≈ 2 minutes)

“The module starts with a clear contrast between two ways of building software.

In a monolithic architecture everything lives in one big package — the user interface, the business logic, and the database access are all tightly bound together. It is easy to start with, but as the system grows it becomes hard to scale specific parts, hard to change technology, and a single bug can take the whole system down.

Microservices take a different approach. We break the system into small, independent services. Each one does one job well, can be developed and deployed on its own, and usually runs inside its own container. The benefits are better scalability, more flexibility for teams, faster releases, and better resilience.

Our project is not a full set of microservices yet. It is one clean, containerized unit. That is actually how most real-world journeys begin — start with a well-packaged independent service, then grow from there.”

---

## Member 3 – Application Logic (≈ 2 minutes)

“The application itself is intentionally straightforward so we could focus on the containerization side.

The user enters four marks: Test 1, Test 2, Assignment 1, and the Project.  
These are weighted 30 %, 50 %, 10 %, and 10 % respectively.

We calculate the final mark and check if it is 50 % or higher. If it is, the student qualifies. If not, they do not.

We also added solid input validation. Anything that is not a number, or is outside the range 0 to 100, is rejected and the program asks again. This stops bad data from ever reaching the calculation.

Even a small program needs clear business rules and defensive coding. Those same habits become critical when the service later sits inside a larger microservices landscape.”

---

## Member 4 – Dockerfile Deep Dive (≈ 2 minutes)

“This is the part we are most proud of.

We used a multi-stage Dockerfile.  
In the first stage we use the full .NET SDK image. We restore packages, compile the code, and publish a Release build.

In the second stage we switch to the much smaller runtime-only image and copy just the published output across.

The result is a lean, secure final image that contains only what is needed to run the application. No compilers, no unnecessary tools.

This is standard practice for production cloud-native services. Smaller images mean faster downloads, fewer security risks, and cleaner deployments.”

---

## Member 1 – Docker Hub & Run Instructions (≈ 90 seconds)

“Once the image was built we pushed it to Docker Hub under the name reneumbra/student-exam-app.

Anyone with Docker installed can now run our application without needing the .NET SDK or even the source code.

The two commands are:

docker pull reneumbra/student-exam-app:latest  
docker run -it --rm reneumbra/student-exam-app:latest

The -it flag keeps the terminal interactive so the user can type marks.  
The --rm flag cleans up the container when it exits.

This is practical proof of portability and distribution — two core cloud-native ideas.”

---

## Live Demo – All Members

**Member 1** starts the container and explains the pull and run commands.

**Member 2** enters a set of marks that produce a passing result and explains the output.

**Member 3** enters a set of marks that produce a failing result.

**Member 4** deliberately types invalid input (letters or numbers outside 0–100) to show the validation working.

After the demo, each person can add one short sentence confirming what was just shown.

---

## Member 2 – Cloud Native Concepts (≈ 90 seconds)

“Even though this is a small project, it already demonstrates several important cloud-native principles:

- Containerization — the app and its runtime travel together  
- Immutability — the image does not change after it is built  
- Portability — it runs the same way on any machine with Docker  
- Declarative configuration — the Dockerfile describes the desired state  
- Distribution through a registry  
- Independence — this calculator can later become one service in a larger system

In a full microservices architecture we could put an API in front of it, run multiple instances, and orchestrate everything with Kubernetes. The foundation is already correct.”

---

## Member 3 – Conclusion (≈ 90 seconds)

“To wrap up, we delivered a working application with correct logic and validation, a clean multi-stage Dockerfile, a public image on Docker Hub, and documentation that lets anyone run it with two commands.

The biggest lessons for us were that packaging and documentation are just as important as the code itself, and that starting with a well-containerized independent unit is the natural first step toward microservices.

Thank you. We are ready for your questions.”

---

## Quick Fallback Lines (if someone freezes)

- “The calculation is a simple weighted average — 30, 50, 10 and 10.”
- “We used a multi-stage build so the final image stays small and secure.”
- “Anyone can run it with just docker pull and docker run.”
- “This is the practical starting point for a microservices architecture.”
