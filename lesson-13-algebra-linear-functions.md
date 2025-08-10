# Lesson 14: Linear Functions

## Concept Introduction

A **linear function** is a function whose graph is a straight line. It represents situations where there's a constant rate of change - meaning the output changes by the same amount each time the input increases by one unit.

The standard form of a linear function is:
**f(x) = mx + b**

Where:
- **m** is the **slope** (rate of change)
- **b** is the **y-intercept** (starting value when x = 0)
- **x** is the input variable
- **f(x)** is the output

Linear functions are everywhere in programming because they model constant rates: download speeds, pricing tiers, resource consumption, and time-based calculations.

## Building Understanding

### The Slope (m) - Rate of Change

The slope tells us how much the output changes when the input increases by 1.

**Positive slope:** Function increases (goes up from left to right)
- f(x) = 3x + 2 has slope 3
- For every 1 unit increase in x, f(x) increases by 3

**Negative slope:** Function decreases (goes down from left to right)  
- f(x) = -2x + 5 has slope -2
- For every 1 unit increase in x, f(x) decreases by 2

**Zero slope:** Function is constant (horizontal line)
- f(x) = 7 has slope 0
- Output never changes regardless of input

### The Y-Intercept (b) - Starting Point

The y-intercept is the output value when the input is zero. It represents the "starting point" or "base amount."

**f(x) = 2x + 50:**
- When x = 0, f(0) = 2(0) + 50 = 50
- The y-intercept is 50
- This might represent a base fee of $50, then $2 per unit

### Reading Linear Functions in Context

**Phone bill:** C(x) = 0.10x + 30
- Base monthly charge: $30 (y-intercept)
- Cost per text: $0.10 (slope)
- If you send 100 texts: C(100) = 0.10(100) + 30 = $40

**Temperature conversion:** F(c) = (9/5)c + 32
- Slope: 9/5 = 1.8 (degrees Fahrenheit per degree Celsius)
- Y-intercept: 32 (freezing point difference)

## Examples

### Example 1: Identifying Slope and Y-Intercept
Given f(x) = 5x - 3, identify the slope and y-intercept.

**Solution:**
Comparing to f(x) = mx + b:
- Slope (m) = 5
- Y-intercept (b) = -3

**Interpretation:** Starting at -3, the function increases by 5 for each unit increase in x.

### Example 2: Writing Linear Functions from Information
A taxi charges $3.50 to start, plus $2.25 per mile. Write a function for the total cost.

**Solution:**
Let C(m) = total cost, where m = miles driven
- Starting fee (y-intercept): $3.50
- Rate per mile (slope): $2.25
- Function: C(m) = 2.25m + 3.50

### Example 3: Finding Slope from Two Points
A function passes through points (1, 7) and (4, 19). Find the slope.

**Solution:**
Slope formula: m = (y₂ - y₁)/(x₂ - x₁)

Using points (1, 7) and (4, 19):
m = (19 - 7)/(4 - 1) = 12/3 = 4

**Interpretation:** The function increases by 4 units for each 1-unit increase in x.

### Example 4: Writing Function from Point and Slope
A linear function has slope -3 and passes through point (2, 8). Find the function.

**Solution:**
Using point-slope form: y - y₁ = m(x - x₁)
y - 8 = -3(x - 2)
y - 8 = -3x + 6
y = -3x + 14

**Function:** f(x) = -3x + 14

**Check:** f(2) = -3(2) + 14 = -6 + 14 = 8 ✓

### Example 5: Parallel and Perpendicular Lines
Given f(x) = 2x + 5, find:
a) A parallel line through (0, -3)
b) A perpendicular line through (0, -3)

**Solutions:**
a) **Parallel lines have the same slope**
   Parallel function: g(x) = 2x - 3

b) **Perpendicular lines have negative reciprocal slopes**
   Original slope: 2, so perpendicular slope: -1/2
   Perpendicular function: h(x) = -½x - 3

### Example 6: Finding Where Lines Intersect
Find where f(x) = 2x + 1 and g(x) = -x + 7 intersect.

**Solution:**
Set functions equal: 2x + 1 = -x + 7
Solve for x: 3x = 6, so x = 2

Find y-coordinate: f(2) = 2(2) + 1 = 5
Or check: g(2) = -2 + 7 = 5 ✓

**Intersection point:** (2, 5)

## 💡 Fun Fact: The Slope Detective

Linear functions help solve real mysteries! Police use them to analyze accident scenes. If skid marks are 60 feet long on dry pavement, they can use the linear relationship between skid distance and speed to determine how fast a car was going before braking.

The function might be: Speed = 5.5 × √(skid_distance)
While this involves a square root, the relationship between speed² and distance is linear!

## 🎯 Try This: The Coffee Shop Economics

A coffee shop's daily profit follows this pattern:
- Fixed costs (rent, utilities): $150 per day
- Profit per coffee sold: $2.75

1. Write a linear function P(c) for daily profit, where c = coffees sold
2. How many coffees must be sold to break even (profit = 0)?
3. What's the profit if they sell 100 coffees?
4. If yesterday's profit was $200, how many coffees were sold?

**Solutions:**

1. **Function:** P(c) = 2.75c - 150
   (Slope = 2.75, y-intercept = -150 because fixed costs reduce profit)

2. **Break-even:** Set P(c) = 0
   0 = 2.75c - 150
   150 = 2.75c
   c = 54.5, so need to sell 55 coffees (round up)

3. **100 coffees:** P(100) = 2.75(100) - 150 = 275 - 150 = $125

4. **Reverse calculation:** If P(c) = 200:
   200 = 2.75c - 150
   350 = 2.75c
   c = 127.3, so about 127 coffees

## 💻 Where You'll See This in Programming

Linear functions are fundamental to programming because they model constant rates and predictable relationships:

**Performance Analysis:**
```python
# Algorithm runtime: T(n) = 0.001n + 5
# 5ms setup time + 0.001ms per data element
def analyze_performance(data_size):
    return 0.001 * data_size + 5
```

**Pricing Calculations:**
```javascript
// SaaS pricing: Cost = $10 base + $2 per user
function calculateMonthlyBill(users) {
    return 2 * users + 10;
}
// Linear function: f(users) = 2users + 10
```

**Memory Management:**
```cpp
// Memory usage: M(objects) = 64 * objects + 1024
// 1KB overhead + 64 bytes per object  
size_t calculateMemoryUsage(int objectCount) {
    return 64 * objectCount + 1024;
}
```

**Graphics and Animation:**
```python
# Linear interpolation between two points
def lerp(start, end, t):
    return start + t * (end - start)
# This is linear function: f(t) = start + (end-start)t

# Position over time: P(t) = initial_pos + velocity * t
def getPosition(time, initial_pos, velocity):
    return initial_pos + velocity * time
```

**Financial Calculations:**
```java
// Simple interest: A(t) = P(1 + rt) = P + Prt  
// Linear in time: A(t) = Pr*t + P
public double calculateSimpleInterest(double principal, double rate, double time) {
    return principal + (principal * rate * time);
}
```

**Resource Scaling:**
```python
# Server capacity planning: Load(users) = 0.05*users + 2
# 2 CPU baseline + 0.05 CPU per user
def calculate_cpu_requirement(concurrent_users):
    return 0.05 * concurrent_users + 2
```

**Game Development:**
```javascript  
// Player experience points: XP(level) = 1000*level + 500
// 500 base XP + 1000 per level
function calculateRequiredXP(level) {
    return 1000 * level + 500;
}
```

**Database Query Optimization:**
```sql
-- Linear search time estimation
-- Time = 0.001 * row_count + 10 (milliseconds)
-- Used for query planning and optimization
```

Understanding linear functions helps you:
- Model and predict constant-rate relationships in code
- Analyze algorithm performance (linear time complexity)
- Implement pricing, billing, and resource calculations
- Create smooth animations and transitions
- Optimize system resource allocation
- Debug performance issues by recognizing linear growth patterns
- Design scalable systems by understanding linear relationships

Linear functions represent the "sweet spot" in programming - predictable, efficient, and easy to understand and debug.

***

**Next Lesson:** We'll explore quadratic functions - relationships that involve squared terms and model acceleration, optimization, and curved relationships in programming.
