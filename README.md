# CNA271 – Student Exam Qualification Calculator

**Belgium Campus | 
Cloud Native Programming 271 |**
---

## Quick Start

1. Open this repository on the presentation machine.
2. Navigate to `docs/presentation/`.
3. Follow the numbered Markdown files in order.
4. For the live demo, open a terminal and run:

```bash
docker pull reneumbra/student-exam-app:latest
docker run -it --rm reneumbra/student-exam-app:latest
```

---

## Repository Structure

```
├── README.md                          ← You are here
├── docs/
│   ├── presentation/                  
│   ├── architecture/                  
│   └── research/                      
├── src/                              
├── Dockerfile
└── LICENSE
```

---

## Group Presentation Roles

| Member | Primary Sections |
|--------|------------------|
| Member 1 | Agenda, Docker Hub, Closing |
| René van der Walt 604356 | Monolithic vs Microservices, Cloud Native Concepts |
| Member 3 | Application Logic, Conclusion |
| Mongezi Mahlangu 605039 | Dockerfile Deep Dive, Live Demo support |

All members participate in the live demonstration.

---

## Project Summary

A simple C# console application that calculates a student’s weighted final mark and decides whether they qualify to write the exam (minimum 50%).

**Weighting**
- Test 1 → 30%
- Test 2 → 50%
- Assignment 1 → 10%
- Project → 10%

The application is fully containerized and published on Docker Hub so anyone can run it with a single command.

---

## How to Run the Application

### Using Docker 

```bash
docker pull reneumbra/student-exam-app:latest
docker run -it --rm reneumbra/student-exam-app:latest
```

### Locally with .NET 10

```bash
cd src
dotnet restore
dotnet run
```

---

## Presentation Package Contents

Everything in the `docs/` folder is designed so the entire presentation can be delivered directly from this GitHub repository. No PowerPoint required.

Open the files in order and follow the speaker notes.
