# Lesson 11: Systems of Equations

## Concept Introduction

A **system of equations** is a set of two or more equations that share the same variables. The solution to a system is the set of values that makes ALL equations true simultaneously.

Think of it like solving a puzzle with multiple clues - you need to find values that satisfy every clue at the same time. In programming terms, it's like finding values that pass multiple validation conditions.

For example:
```
x + y = 10
2x - y = 2
```

We need to find values of x and y that make both equations true at the same time.

## Building Understanding

### What Does "Simultaneous" Mean?

When we solve a single equation like x + 5 = 12, there's one answer: x = 7.

But with systems, we're looking for the intersection point - where all equations agree. This might result in:
- **One unique solution** (lines intersect at one point)
- **No solution** (parallel lines never meet)
- **Infinite solutions** (same line written differently)

### Visualizing Systems

Each linear equation represents a straight line on a graph. The solution to the system is where these lines intersect:

```
x + y = 10    (line 1)
2x - y = 2    (line 2)
```

These lines cross at exactly one point: (4, 6). We can verify:
- Line 1: 4 + 6 = 10 ✓
- Line 2: 2(4) - 6 = 8 - 6 = 2 ✓

## Two Main Solution Methods

### Method 1: Substitution

**Steps:**
1. Solve one equation for one variable
2. Substitute that expression into the other equation
3. Solve for the remaining variable
4. Substitute back to find the first variable
5. Check both equations

### Method 2: Elimination

**Steps:**
1. Multiply equations to make coefficients of one variable opposite
2. Add equations to eliminate that variable
3. Solve for the remaining variable
4. Substitute back to find the first variable
5. Check both equations

## Examples

### Example 1: Substitution Method
Solve:
```
x + y = 10
2x - y = 2
```

**Solution:**
Step 1: Solve the first equation for y
y = 10 - x

Step 2: Substitute into the second equation
2x - (10 - x) = 2
2x - 10 + x = 2
3x - 10 = 2
3x = 12
x = 4

Step 3: Find y using x = 4
y = 10 - 4 = 6

**Solution: (4, 6)**

**Check:**
- Equation 1: 4 + 6 = 10 ✓
- Equation 2: 2(4) - 6 = 8 - 6 = 2 ✓

### Example 2: Elimination Method
Solve:
```
3x + 2y = 16
5x - 2y = 8
```

**Solution:**
Notice the y coefficients are already opposites (+2y and -2y).

Step 1: Add the equations
```
3x + 2y = 16
5x - 2y = 8
___________
8x + 0y = 24
```

Step 2: Solve for x
8x = 24
x = 3

Step 3: Substitute x = 3 into either original equation
3(3) + 2y = 16
9 + 2y = 16
2y = 7
y = 3.5

**Solution: (3, 3.5)**

**Check:**
- Equation 1: 3(3) + 2(3.5) = 9 + 7 = 16 ✓
- Equation 2: 5(3) - 2(3.5) = 15 - 7 = 8 ✓

### Example 3: Elimination with Multiplication
Solve:
```
2x + 3y = 7
4x + 5y = 13
```

**Solution:**
To eliminate x, multiply the first equation by -2:
```
-4x - 6y = -14
4x + 5y = 13
______________
0x - y = -1
```

So y = 1

Substitute y = 1 into the first equation:
2x + 3(1) = 7
2x + 3 = 7
2x = 4
x = 2

**Solution: (2, 1)**

### Example 4: No Solution
Solve:
```
x + 2y = 5
x + 2y = 8
```

**Analysis:**
These equations say the same expression (x + 2y) equals two different values (5 and 8). This is impossible, so there's no solution. The lines are parallel and never intersect.

### Example 5: Infinite Solutions
Solve:
```
2x + 4y = 10
x + 2y = 5
```

**Analysis:**
If we multiply the second equation by 2, we get:
2x + 4y = 10

This is identical to the first equation! These are the same line written differently, so every point on the line is a solution. There are infinite solutions.

## 🎯 Try This: The Fruit Stand Problem

At a fruit stand:
- 2 apples and 3 oranges cost $7
- 1 apple and 2 oranges cost $4

Find the cost of one apple and one orange.

**Set up the system:**
Let a = cost of one apple, o = cost of one orange
- 2a + 3o = 7
- 1a + 2o = 4

**Solve using your preferred method:**
1. Try substitution first
2. Then try elimination
3. Which method felt easier for this problem?

**Solution:** Apple costs $2, orange costs $1
**Check:** 2($2) + 3($1) = $4 + $3 = $7 ✓ and 1($2) + 2($1) = $2 + $2 = $4 ✓

## 💻 Where You'll See This in Programming

Systems of equations are everywhere in programming, often hidden within complex problems:

**Computer Graphics:**
```
// Finding intersection of two lines for collision detection
// Line 1: y = 2x + 3
// Line 2: y = -x + 9
// Solve: 2x + 3 = -x + 9 to find intersection point
```

**GPS and Navigation:**
```
// GPS calculates position by solving system of equations from satellite signals
// Each satellite provides one equation based on distance
// Need at least 3 satellites (3 equations) to find 2D position
```

**Network Flow and Resource Allocation:**
```
// Balancing server loads
// Server A: 2x + 3y ≤ 100 (capacity constraint)  
// Server B: x + 2y ≤ 60 (capacity constraint)
// Minimize cost: 5x + 3y (objective function)
```

**Game Development:**
```
// Physics simulations - when do two moving objects collide?
// Object 1 position: x₁ = 10 + 5t, y₁ = 20 + 3t
// Object 2 position: x₂ = 50 - 2t, y₂ = 5 + 7t  
// Collision when x₁ = x₂ AND y₁ = y₂ (system of equations)
```

**Machine Learning:**
```
// Linear regression finds the best line through data points
// Solved by system: minimize sum of squared errors
// Results in normal equations (system of linear equations)
```

**Cryptography:**
```
// Some encryption methods rely on solving systems
// RSA key generation involves solving modular equations
// Error correction codes use linear algebra (systems of equations)
```

**Economics and Business:**
```
// Break-even analysis
// Revenue: R = 50x (price × quantity)
// Cost: C = 30x + 1000 (variable cost + fixed cost)
// Break-even when R = C: solve 50x = 30x + 1000
```

Understanding systems of equations helps you:
- Model real-world constraints with multiple conditions
- Solve optimization problems in algorithms
- Debug complex mathematical relationships in code
- Understand how linear algebra libraries work
- Design algorithms that find optimal solutions under multiple constraints

Many advanced programming concepts (linear programming, machine learning, computer graphics) are built on the foundation of solving systems of equations efficiently.

***

**Next Lesson:** We'll explore inequalities - mathematical statements that describe ranges and constraints rather than exact equality.
