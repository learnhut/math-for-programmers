# Lesson 13: Functions as Mathematical Relationships

## Concept Introduction

A **mathematical function** is a special relationship between inputs and outputs where each input produces exactly one output. Think of a function as a machine: you put something in, the machine processes it according to a rule, and exactly one thing comes out.

The key characteristic of a function is this "one input, one output" rule. If you put the same input into a function multiple times, you'll always get the same output.

We write functions using **function notation**: f(x) = 2x + 3
- f is the name of the function
- x is the input (called the **independent variable**)
- 2x + 3 is the rule that transforms the input
- The result is the output (called the **dependent variable**)

## Building Understanding

### Function as a Process

Think of these real-world examples of functions:
- **Vending machine:** Input money → Output snack
- **Calculator:** Input numbers → Output result  
- **Recipe:** Input ingredients → Output meal
- **Your phone:** Input contact name → Output phone number

In each case, the same input always produces the same output.

### Function Notation Explained

**f(x) = x²** means:
- The function is named "f"
- The input variable is "x" 
- The rule is "square the input"
- f(3) = 3² = 9
- f(-2) = (-2)² = 4

**g(t) = 5t - 7** means:
- The function is named "g"
- The input variable is "t"
- The rule is "multiply by 5, then subtract 7"
- g(4) = 5(4) - 7 = 20 - 7 = 13

### Domain and Range

**Domain:** All possible input values that make sense for the function
- For f(x) = x + 5, domain is all real numbers
- For f(x) = 1/x, domain is all real numbers except x = 0
- For f(x) = √x, domain is x ≥ 0 (can't take square root of negatives)

**Range:** All possible output values the function can produce
- For f(x) = x², range is y ≥ 0 (squares are never negative)
- For f(x) = 3, range is just {3} (constant function)

### Function vs Not a Function

**This IS a function:**
```
Input → Output
1 → 5
2 → 7  
3 → 9
4 → 11
```
Each input has exactly one output.

**This is NOT a function:**
```
Input → Output
1 → 5
2 → 7
2 → 9    ← Problem! Input 2 has two different outputs
3 → 11
```

## Examples

### Example 1: Evaluating Functions
Given f(x) = 3x - 4, find f(5).

**Solution:**
f(5) = 3(5) - 4 = 15 - 4 = 11

### Example 2: Multiple Evaluations
Given g(x) = x² + 2x - 1, find:
a) g(0)
b) g(-3)
c) g(2)

**Solutions:**
a) g(0) = (0)² + 2(0) - 1 = 0 + 0 - 1 = -1
b) g(-3) = (-3)² + 2(-3) - 1 = 9 - 6 - 1 = 2  
c) g(2) = (2)² + 2(2) - 1 = 4 + 4 - 1 = 7

### Example 3: Function with Variables as Input
Given h(x) = 2x + 5, find h(a + 1).

**Solution:**
h(a + 1) = 2(a + 1) + 5 = 2a + 2 + 5 = 2a + 7

### Example 4: Function Composition
Given f(x) = x + 3 and g(x) = 2x, find f(g(4)).

**Solution:**
Step 1: Find g(4)
g(4) = 2(4) = 8

Step 2: Find f(8)
f(8) = 8 + 3 = 11

Therefore, f(g(4)) = 11

### Example 5: Writing Functions from Word Problems
"The cost of renting a car is $25 per day plus $0.15 per mile driven."

**Solution:**
Let d = number of days, m = number of miles
Cost function: C(d,m) = 25d + 0.15m

Or if we only consider miles (assuming 1 day):
C(m) = 25 + 0.15m

### Example 6: Determining Domain
Find the domain of f(x) = √(x - 2).

**Solution:**
For the square root to be defined, we need:
x - 2 ≥ 0
x ≥ 2

Domain: x ≥ 2 or [2, ∞)

## 🎯 Try This: The Phone Plan Function

A cell phone plan charges $30 per month plus $0.10 for each text message over 500.

1. Write a function T(x) that gives the total monthly cost, where x is the number of texts sent
2. What's the domain of this function in real life?
3. Calculate T(500), T(750), and T(1200)
4. If someone's bill is $45, how many texts did they send?

**Solutions:**

1. **Function:** T(x) = 30 + 0.10(x - 500) for x > 500, and T(x) = 30 for x ≤ 500

2. **Domain:** x ≥ 0 (can't send negative texts) and x must be a whole number

3. **Evaluations:**
   - T(500) = 30 (no extra charge)
   - T(750) = 30 + 0.10(750 - 500) = 30 + 0.10(250) = 30 + 25 = $55
   - T(1200) = 30 + 0.10(1200 - 500) = 30 + 0.10(700) = 30 + 70 = $100

4. **Reverse calculation:** If T(x) = 45:
   45 = 30 + 0.10(x - 500)
   15 = 0.10(x - 500)
   150 = x - 500
   x = 650 texts

## 💻 Where You'll See This in Programming

Mathematical functions are the foundation of programming functions - they share the same core concept but are used in different contexts:

**Function Similarities:**
```python
# Mathematical: f(x) = 2x + 3
def f(x):
    return 2 * x + 3

# Same input always gives same output
print(f(5))  # Always outputs 13
print(f(5))  # Always outputs 13
```

**Real Programming Applications:**

**Data Processing Functions:**
```javascript
// Convert temperature: F(c) = (9/5)c + 32
function celsiusToFahrenheit(celsius) {
    return (9/5) * celsius + 32;
}

// Domain: all real numbers
// Range: all real numbers
```

**Business Logic Functions:**
```python
# Tax calculation: T(income) = income * rate
def calculateTax(income, rate=0.25):
    if income <= 0:  # Domain restriction
        return 0
    return income * rate
```

**Game Development Functions:**
```cpp
// Player score: S(level, time) = level * 100 - time * 5  
int calculateScore(int level, int timeSeconds) {
    return level * 100 - timeSeconds * 5;
}
```

**Graphics and Animation:**
```python
# Position function: P(t) = initial_pos + velocity * t
def getPosition(time, initial_pos, velocity):
    return initial_pos + velocity * time

# Domain: t ≥ 0 (time can't be negative)
```

**Database Query Functions:**
```sql
-- Price calculation: P(quantity) = quantity * unit_price * (1 - discount)
CREATE FUNCTION calculatePrice(quantity INT, unit_price DECIMAL, discount DECIMAL)
RETURNS DECIMAL
AS quantity * unit_price * (1 - discount);
```

**API Response Functions:**
```javascript
// User profile: U(userId) → {name, email, preferences}
async function getUserProfile(userId) {
    // Same userId always returns same profile (at that moment)
    return await database.findUser(userId);
}
```

Understanding mathematical functions helps you:
- Design predictable, testable code functions
- Understand function composition and chaining
- Recognize when functions should be pure (same input → same output)
- Model real-world relationships mathematically in your code
- Debug function behavior by tracing inputs through transformations
- Optimize functions by understanding their mathematical properties
- Choose appropriate domains and handle edge cases properly

The mathematical concept of "one input, one output" is crucial for writing reliable, debuggable code functions.

***

**Next Lesson:** We'll explore linear functions specifically - the simplest type of function that models constant rates of change and appears everywhere in programming.
