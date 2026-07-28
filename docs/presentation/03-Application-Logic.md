# 3. Application Logic

The program is deliberately simple so the focus stays on containerization and cloud-native practices.

### What the user does

1. Enters Test 1 mark (out of 100)
2. Enters Test 2 mark (out of 100)
3. Enters Assignment 1 mark (out of 100)
4. Enters Project mark (out of 100)

### Calculation

```
Final Mark = (Test1 × 0.30) + (Test2 × 0.50) + (Assignment1 × 0.10) + (Project × 0.10)
```

### Decision

- If Final Mark ≥ 50 → Student QUALIFIES
- If Final Mark < 50 → Student DOES NOT QUALIFY

### Input validation

We reject anything that is:
- Not a number
- Below 0
- Above 100

The program keeps asking until it gets a valid mark.  
This prevents bad data from entering the calculation.

### Why this matters

Even a small console application needs clear business rules and defensive coding.  
These same habits become critical when the service later becomes part of a larger microservices landscape.
