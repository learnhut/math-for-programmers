# Lesson 10: Solving Linear Equations

## Concept Introduction

A **linear equation** is an equation where the variable appears only to the first power (no squares, cubes, or other exponents). Linear equations represent straight-line relationships and are the foundation of algebraic problem-solving.

The goal when solving an equation is to find the value of the variable that makes the equation true. We do this by **isolating the variable** - getting it alone on one side of the equals sign.

The key principle: **Whatever you do to one side of an equation, you must do to the other side.** Think of an equation like a perfectly balanced scale - to keep it balanced, any change to one side must be matched on the other side.

## Building Understanding

### The Balance Method

Imagine an equation as a balanced scale:
```
x + 5 = 12
```

To solve this, we need to remove the "+5" from the left side. To keep the scale balanced, we subtract 5 from both sides:

```
x + 5 - 5 = 12 - 5
x = 7
```

### Types of Linear Equations

**One-step equations**: Require only one operation to solve
- x + 7 = 15  (subtract 7 from both sides)
- 3x = 21    (divide both sides by 3)
- x/4 = 6    (multiply both sides by 4)

**Two-step equations**: Require two operations to solve
- 2x + 3 = 11  (subtract 3, then divide by 2)
- 5x - 7 = 18  (add 7, then divide by 5)

**Multi-step equations**: May require combining like terms or distributing first
- 3x + 2x = 25     (combine like terms first)
- 2(x + 4) = 18    (distribute first)

### The Standard Strategy

1. **Simplify both sides** (combine like terms, distribute)
2. **Get variables on one side** (add or subtract variable terms)
3. **Get constants on the other side** (add or subtract numbers)
4. **Isolate the variable** (multiply or divide)
5. **Check your answer** (substitute back into original equation)

## Examples

### Example 1: One-Step Equation
Solve: x - 8 = 15

**Solution:**
Add 8 to both sides:
x - 8 + 8 = 15 + 8
x = 23

**Check:** 23 - 8 = 15 ✓

### Example 2: Another One-Step Equation
Solve: 6x = 42

**Solution:**
Divide both sides by 6:
6x ÷ 6 = 42 ÷ 6
x = 7

**Check:** 6(7) = 42 ✓

### Example 3: Two-Step Equation
Solve: 3x + 5 = 20

**Solution:**
Step 1: Subtract 5 from both sides
3x + 5 - 5 = 20 - 5
3x = 15

Step 2: Divide both sides by 3
3x ÷ 3 = 15 ÷ 3
x = 5

**Check:** 3(5) + 5 = 15 + 5 = 20 ✓

### Example 4: Equation with Variables on Both Sides
Solve: 5x - 3 = 2x + 9

**Solution:**
Step 1: Subtract 2x from both sides
5x - 2x - 3 = 2x - 2x + 9
3x - 3 = 9

Step 2: Add 3 to both sides
3x - 3 + 3 = 9 + 3
3x = 12

Step 3: Divide both sides by 3
x = 4

**Check:** 5(4) - 3 = 20 - 3 = 17, and 2(4) + 9 = 8 + 9 = 17 ✓

### Example 5: Equation with Fractions
Solve: x/3 + 2 = 8

**Solution:**
Step 1: Subtract 2 from both sides
x/3 = 6

Step 2: Multiply both sides by 3
x = 18

**Check:** 18/3 + 2 = 6 + 2 = 8 ✓

## 🎯 Try This: The Age Puzzle

Sarah is thinking of her age. She gives you this clue:

"If you take my age, multiply it by 3, then subtract 12, you get 21."

**Your turn:**
1. Set up the equation using x for Sarah's age
2. Solve step by step
3. Check your answer by substituting back
4. How old is Sarah?

**Solution process:**
- Equation: 3x - 12 = 21
- Add 12: 3x = 33  
- Divide by 3: x = 11
- Check: 3(11) - 12 = 33 - 12 = 21 ✓
- Sarah is 11 years old!

Now create your own age puzzle using a different mathematical operation, and challenge someone to solve it.

## 💻 Where You'll See This in Programming

Linear equations appear constantly in programming, often disguised as formulas you need to rearrange or as problems you need to solve algorithmically:

**Game Development:**
```
// Finding when two moving objects meet
// Player position: 10 + 5t
// Enemy position: 100 - 3t  
// When do they meet? 10 + 5t = 100 - 3t
// Solve: 8t = 90, so t = 11.25 seconds
```

**Financial Calculations:**
```
// Loan payment formula: P = L[c(1 + c)^n]/[(1 + c)^n - 1]
// Often need to solve for different variables (L, c, or n)
```

**Physics Simulations:**
```
// Projectile motion: y = v₀t - (1/2)gt²
// Finding when object hits ground: 0 = v₀t - (1/2)gt²
// Solve for t to find flight time
```

**Algorithm Optimization:**
```
// Finding break-even points between different algorithms
// Algorithm A: 5n + 100 operations
// Algorithm B: 2n + 500 operations  
// When is A faster? Solve: 5n + 100 < 2n + 500
```

**User Interface:**
```
// Responsive design calculations
// Container width = margin + content + padding
// Need to solve for content width given total width
```

Understanding equation solving helps you:
- Rearrange formulas to solve for different variables
- Debug mathematical calculations in code
- Optimize algorithms by finding critical points
- Convert word problems into solvable code logic
- Validate that your mathematical models work correctly

The step-by-step logical thinking you use to solve equations is exactly the same process you use to debug code and trace through algorithm execution.

***

**Next Lesson:** We'll learn how to solve multiple equations simultaneously - a crucial skill for handling complex programming problems with multiple unknown values.
