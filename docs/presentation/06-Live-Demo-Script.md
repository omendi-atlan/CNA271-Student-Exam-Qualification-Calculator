# 6. Live Demonstration Script

**Goal:** Show the application working correctly, including validation and both pass/fail outcomes.

### Preparation
Open a terminal and make sure Docker is running.

### Step-by-step (rotate speakers)

**Member 1**
```bash
docker pull reneumbra/student-exam-app:latest
docker run -it --rm reneumbra/student-exam-app:latest
```
Explain: “We are pulling the exact image we published and starting it interactively.”

**Member 2 – Qualifying student**
Enter marks that produce a final mark ≥ 50, for example:
- Test 1: 65
- Test 2: 58
- Assignment 1: 80
- Project: 90

Expected result: Final Mark around 65.5% → QUALIFIES

**Member 3 – Non-qualifying student**
Enter lower marks, for example:
- Test 1: 40
- Test 2: 35
- Assignment 1: 50
- Project: 45

Expected result: Final Mark below 50% → DOES NOT QUALIFY

**Member 4 – Validation**
Deliberately enter invalid input:
- 150
- abc
- -10

Show that the program rejects the input and asks again.

### After the demo
All members briefly confirm:
- The calculation is correct
- Validation works
- The container behaved exactly as documented
