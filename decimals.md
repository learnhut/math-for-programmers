# Episode 4: Decimals and Place Value

*Duration: 22-25 minutes*

## Concept Introduction (4 minutes)

Every time you handle money in code ($12.99), work with GPS coordinates (40.7128° N), or calculate percentages (87.5%), you're using decimals. But decimals are more than just "numbers with dots" - they're an extension of our place value system that lets us represent parts of wholes with incredible precision.

Understanding how decimals work mathematically is crucial for programming because it explains why some calculations give unexpected results (like 0.1 + 0.2 ≠ 0.3) and helps you choose the right data types for accurate computations.

## Building Understanding (15 minutes)

### The Place Value System Extended

You already know whole number place values:

| Thousands | Hundreds | Tens | Ones |
|-----------|----------|------|------|
| 1000      | 100      | 10   | 1    |

Decimals extend this pattern to the right:

| Ones | . | Tenths | Hundredths | Thousandths |
|------|---|--------|------------|-------------|
| 1    | . | 1/10   | 1/100      | 1/1000      |
| 1    | . | 0.1    | 0.01       | 0.001       |

**Example: 42.573**
- 4 in the tens place = 40
- 2 in the ones place = 2  
- 5 in the tenths place = 5/10 = 0.5
- 7 in the hundredths place = 7/100 = 0.07
- 3 in the thousandths place = 3/1000 = 0.003
- Total: 40 + 2 + 0.5 + 0.07 + 0.003 = 42.573

### Converting Fractions to Decimals

**Method: Long Division**

Convert 3/4 to decimal:
```
3 ÷ 4 = 0.75

   0.75
4)3.00
   2.8
   ---
   0.20
   0.20
   ---
   0.00
```

Convert 1/3 to decimal:
```
1 ÷ 3 = 0.333...

   0.333...
3)1.000...
   0.9
   ---
   0.10
   0.09
   ---
   0.010
   0.009
   ---
   0.001... (continues forever)
```

### Terminating vs Non-Terminating Decimals

**Terminating decimals** end after a finite number of digits:
- 1/2 = 0.5 ✓
- 3/4 = 0.75 ✓  
- 7/8 = 0.875 ✓

**Non-terminating (repeating) decimals** go on forever:
- 1/3 = 0.333... (repeats 3)
- 1/7 = 0.142857142857... (repeats 142857)
- 22/7 = 3.142857142857... (π approximation)

### Why Some Fractions Become Infinite Decimals

A fraction gives a terminating decimal only if its denominator (in lowest terms) has prime factors of only 2 and/or 5.

**Why 2 and 5?** Because our decimal system is base 10, and 10 = 2 × 5.

**Examples:**
- 1/4 = 1/(2²) = 0.25 ✓ (only factor 2)
- 1/5 = 0.2 ✓ (only factor 5)  
- 1/8 = 1/(2³) = 0.125 ✓ (only factor 2)
- 1/10 = 1/(2×5) = 0.1 ✓ (factors 2 and 5)

- 1/3 = 0.333... ✗ (factor 3, not 2 or 5)
- 1/6 = 1/(2×3) = 0.1666... ✗ (has factor 3)
- 1/7 = 0.142857... ✗ (factor 7, not 2 or 5)

### Rounding and Precision

**Rounding Rules:**
- If the digit after your rounding place is 5 or greater, round up
- If it's 4 or less, round down

**Examples:**
- 3.147 rounded to 2 decimal places = 3.15 (7 ≥ 5, round up)
- 3.143 rounded to 2 decimal places = 3.14 (3 < 5, round down)
- 2.685 rounded to 2 decimal places = 2.69 (5 ≥ 5, round up)

**Precision vs Accuracy:**
- **Precision**: How many decimal places you show
- **Accuracy**: How close to the true value you are

You can be precise but not accurate (3.14159265 for π when you meant 3.2), or accurate but not precise (3.1 for π).

## 💡 Fun Fact: The 1/7 Mystery (3 minutes)

Calculate 1/7 as a decimal by hand using long division. Keep going for at least 12 decimal places:

```
1 ÷ 7 = 0.142857142857142857...
```

You'll discover that the same 6 digits (142857) repeat forever! This is called the "repetend" of 1/7.

**Even more amazing:**
- 2/7 = 0.285714285714... (same digits, different starting point!)
- 3/7 = 0.428571428571... (same digits, different starting point!)
- 4/7 = 0.571428571428... (same digits, different starting point!)

All fractions with 7 in the denominator share the same repeating pattern, just starting at different positions. This happens because of the mathematical properties of division and remainders!

**Try this with 1/3, 1/9, 2/7 - each fraction has its own unique repeating signature.**

## 💻 Where You'll See This in Programming (4 minutes)

**Floating-Point Precision Issues:**
```python
# This might surprise you!
result = 0.1 + 0.2
print(result)  # Outputs: 0.30000000000000004 (not exactly 0.3!)
```

**Why this happens:** Computers store decimals in binary (base 2), but some decimals that are exact in base 10 become repeating decimals in base 2. Just like 1/3 can't be exactly represented in decimal, 0.1 can't be exactly represented in binary.

**Currency Calculations:**
```python
# Wrong way (floating point errors)
price = 0.1 + 0.2  # Might not equal 0.3 exactly

# Right way (use integers for cents)
price_cents = 10 + 20  # 30 cents exactly
price_dollars = price_cents / 100  # Convert to dollars when displaying
```

**GPS Coordinates and Precision:**
```python
latitude = 40.7128  # 4 decimal places ≈ 11 meter accuracy
longitude = -74.0060

# More precision = more accuracy
precise_lat = 40.712800  # 6 decimal places ≈ 0.1 meter accuracy
```

**Progress and Percentages:**
```python
completed = 127
total = 200
percentage = (completed / total) * 100  # 63.5%
display = round(percentage, 1)  # Show as 63.5%
```

**Graphics and Animation:**
```python
# Smooth animation requires decimal positions
player_x = 100.0
movement_speed = 2.5  # pixels per frame
player_x += movement_speed  # Now at 102.5
```

**Scientific Computing:**
```python
# High precision calculations
import decimal
decimal.getcontext().prec = 50  # 50 decimal places of precision

# For exact decimal arithmetic
from decimal import Decimal
exact = Decimal('0.1') + Decimal('0.2')  # Exactly 0.3
```

Understanding decimal mathematics helps you:
- Choose appropriate data types (float vs double vs decimal)
- Avoid rounding errors in financial calculations
- Set proper precision for scientific computations
- Debug unexpected calculation results

**Performance Tip:** Integer arithmetic is faster than decimal arithmetic. When possible, work with integers (like cents instead of dollars) and convert to decimals only for display.
