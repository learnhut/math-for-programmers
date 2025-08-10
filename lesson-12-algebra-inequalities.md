# Lesson 12: Inequalities

## Concept Introduction

An **inequality** is a mathematical statement that compares two expressions using symbols other than equals. Instead of saying two things are exactly equal, inequalities tell us about relationships like "greater than," "less than," or "at most."

The inequality symbols are:
- **>** means "greater than"
- ** 5** reads as "x is greater than 5"
- This means x could be 6, 7, 10, 100, or any number larger than 5
- But x cannot be 5, 4, 3, or any number less than or equal to 5

**y ≤ -2** reads as "y is less than or equal to negative 2"
- This means y could be -2, -3, -10, -100, or any number less than or equal to -2
- But y cannot be -1, 0, 5, or any number greater than -2

### Inequality vs Equation Solutions

**Equation:** x + 3 = 7 has one solution: x = 4
**Inequality:** x + 3 > 7 has infinitely many solutions: x > 4 (x could be 5, 6, 7, 8, 100, etc.)

### Graphing Inequalities on Number Lines

We use number lines to visualize inequality solutions:

**For x > 3:**
- Draw an open circle at 3 (since 3 is not included)
- Shade everything to the right of 3

**For x ≤ -1:**
- Draw a filled circle at -1 (since -1 is included)
- Shade everything to the left of -1

## Solving Inequalities

The rules for solving inequalities are almost identical to solving equations, with one crucial exception:

### The Golden Rule of Inequalities

**When you multiply or divide both sides by a negative number, you must flip the inequality sign.**

Why? Consider: 5 > 2 (true)
Multiply both sides by -1: -5 ? -2
Since -5 is less than -2, we get: -5  12

**Solution:**
Subtract 7 from both sides:
x + 7 - 7 > 12 - 7
x > 5

**Answer:** All numbers greater than 5

### Example 2: Inequality with Division
Solve: 3x ≤ 15

**Solution:**
Divide both sides by 3:
3x ÷ 3 ≤ 15 ÷ 3
x ≤ 5

**Answer:** All numbers less than or equal to 5

### Example 3: Negative Coefficient (Sign Flip!)
Solve: -2x > 8

**Solution:**
Divide both sides by -2 (and flip the inequality sign):
-2x ÷ (-2)  8

**Solution:**
Solve each inequality separately:

Part 1: x - 2  8
x > 5

**Answer:** x  5 (numbers less than -3 or numbers greater than 5)

## 🎯 Try This: The Temperature Problem

A recipe calls for baking at a temperature between 325°F and 375°F, inclusive.

1. Write this as a compound inequality using T for temperature
2. If you have an oven that reads in Celsius, convert the constraint
   (Remember: F = (9/5)C + 32)
3. What's the allowed temperature range in Celsius?

**Setup:** 325 ≤ T ≤ 375

**For Celsius conversion:**
325 ≤ (9/5)C + 32 ≤ 375

**Solve the compound inequality:**
- Subtract 32: 293 ≤ (9/5)C ≤ 343
- Multiply by 5/9: 162.8 ≤ C ≤ 190.6

**Answer:** Between approximately 163°C and 191°C

## 💻 Where You'll See This in Programming

Inequalities are fundamental to programming logic and appear constantly in conditional statements, validation, and algorithm design:

**Input Validation:**
```javascript
// Age validation for website registration
if (age >= 13 && age  1000):
    useOptimizedAlgorithm()
else:
    useSimpleAlgorithm()
```

**Game Development:**
```cpp
// Player health system
if (health = 650 && income > 50000 && debtRatio  target):
        right = mid - 1
# Inequalities control the search space
```

**Resource Management:**
```c
// Memory allocation limits
if (requestedMemory  100):
    throttleUser()
elif (requestsPerMinute > 500):
    blockUser()
```

**Database Queries:**
```sql
-- Find products in price range
SELECT * FROM products 
WHERE price >= 10.00 AND price <= 50.00;
-- Direct translation of compound inequality
```

Understanding inequalities helps you:
- Write robust conditional logic that handles edge cases
- Design proper validation systems
- Implement algorithm constraints and bounds checking
- Debug range-related errors in code
- Optimize performance by using inequality-based shortcuts
- Create meaningful business rules in applications

The logical thinking required for inequality solving directly translates to writing conditional statements and handling ranges in programming.

***

**Next Lesson:** We'll explore functions as mathematical relationships - the foundation for understanding how inputs transform into outputs in both mathematics and programming.
