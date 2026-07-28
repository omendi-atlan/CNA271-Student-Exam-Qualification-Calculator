# 1. Introduction & Project Overview

Good morning / afternoon everyone.

We are presenting our CNA271 project: a containerized Student Exam Qualification Calculator.

The assignment asked us to:

- Build a console application that decides whether a student qualifies to write the exam
- Use a weighted average of four assessments
- Create a Dockerfile
- Publish the image to Docker Hub
- Provide clear documentation so anyone can run it with the Docker CLI
- Demonstrate the whole thing

We chose C# and .NET 10 because it is clean, modern, and well supported by official Microsoft container images.

The core idea is simple but important:

A student qualifies only if their final weighted mark is **50% or higher**.

**Weights used:**
- Test 1 → 30%
- Test 2 → 50%
- Assignment 1 → 10%
- Project → 10%

This small application is our practical first step into cloud-native thinking.  
Even though it is a single console app right now, it is already packaged as an independent, portable, immutable unit that can run anywhere Docker is available.

That is the foundation of microservices.
