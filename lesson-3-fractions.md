# Episode 3: Fractions - Parts of Wholes

*Duration: 22-25 minutes*

## Concept Introduction (4 minutes)

Fractions represent parts of a whole - something that can't be expressed with whole numbers alone. When you resize an image to half its width, calculate a progress bar at 3/4 complete, or deal with frame rates like 1/60th of a second, you're working with fractions.

Understanding fractions mathematically is crucial for programming because they give you precise control over ratios, proportions, and divisions that decimals sometimes can't represent exactly.

## Building Understanding (14 minutes)

### What Fractions Actually Represent

A fraction has two parts:
- **Numerator** (top): How many parts you have
- **Denominator** (bottom): How many parts make the whole

**Examples:**
- 3/4 = 3 parts out of 4 total parts
- 7/10 = 7 parts out of 10 total parts  
- 1/2 = 1 part out of 2 total parts (half)

### Visualizing Fractions

Think of a pizza cut into 8 equal slices:
- The whole pizza = 8/8
- Half the pizza = 4/8
- One slice = 1/8
- Three slices = 3/8

### Equivalent Fractions: Same Value, Different Names

These all represent the same amount:
- 1/2 = 2/4 = 3/6 = 4/8 = 50/100

**Why are they equivalent?**
When you multiply or divide both numerator and denominator by the same number, the value stays the same:

1/2 × 2/2 = 2/4 (multiplied both by 2)
6/8 ÷ 2/2 = 3/4 (divided both by 2)

### Adding and Subtracting Fractions

**Same denominator (easy case):**
- 2/7 + 3/7 = 5/7 (just add numerators)
- 5/8 - 2/8 = 3/8 (just subtract numerators)

**Different denominators (need common ground):**
- 1/4 + 1/6 = ?
- Find common denominator: 4 and 6 both go into 12
- 1/4 = 3/12 and 1/6 = 2/12
- 3/12 + 2/12 = 5/12

### Multiplying Fractions

Multiply straight across:
- 2/3 × 4/5 = (2×4)/(3×5) = 8/15

**Why this works:**
2/3 of 4/5 means "take 2/3 of something that's already 4/5"
- 4/5 cut into 3 equal parts = 4/15 each
- Take 2 of those parts = 2 × 4/15 = 8/15

### Dividing Fractions

"Flip and multiply" - multiply by the reciprocal:
- 3/4 ÷ 2/5 = 3/4 × 5/2 = 15/8

**Why this works:**
"How many 2/5's fit into 3/4?" is the same as "3/4 × how many make one 2/5?"
Since 5/2 makes one 2/5, we multiply: 3/4 × 5/2

### Proper vs Improper Fractions

**Proper fraction:** Numerator smaller than denominator
- 3/4, 2/5, 7/10 (all less than 1 whole)

**Improper fraction:** Numerator larger than or equal to denominator  
- 5/4, 7/3, 9/9 (greater than or equal to 1 whole)
- Can be written as mixed numbers: 5/4 = 1¼

## 🎯 Try This: The Pizza Problem (3 minutes)

Cut a circular piece of paper into 8 equal slices. Now try to divide it equally among 3 people. What fraction does each person get?

**Solution:**
- Total slices: 8
- People: 3  
- Each person gets: 8/3 slices
- That's 2⅔ slices each (2 whole slices + 2/3 of another slice)

Try the same with 6 slices, 10 slices. Notice:
- 6 ÷ 3 = 2 (divides evenly)
- 10 ÷ 3 = 3⅓ (doesn't divide evenly)

Numbers that divide evenly into the total give whole number results. Others require fractions!

## 💻 Where You'll See This in Programming (4 minutes)

**Progress Bars and Loading:**
```python
completed_tasks = 3
total_tasks = 4
progress = completed_tasks / total_tasks  # 3/4 = 0.75 = 75%
```

**Image and UI Scaling:**
```python
original_width = 800
scale_factor = 1/2  # Resize to half width
new_width = original_width * scale_factor  # 400 pixels
```

**Frame Rates and Timing:**
```python
fps = 60  # frames per second
frame_time = 1/60  # Each frame is 1/60th of a second
total_time = frame_time * frame_count
```

**Aspect Ratios:**
```python
# 16:9 aspect ratio = 16/9 ≈ 1.78
screen_width = 1920
screen_height = 1080
aspect_ratio = screen_width / screen_height  # 16/9
```

**Memory and Resource Allocation:**
```python
total_memory = 8  # GB
allocated = 3/8   # 3/8 of total memory
memory_used = total_memory * allocated  # 3 GB
```

**Precision vs Decimals:**
Fractions can represent exact values that decimals cannot:
- 1/3 as a decimal = 0.333... (repeating forever)
- 1/3 as a fraction = exactly 1/3 (perfectly precise)

This is why financial software often uses fractions internally instead of decimals to avoid rounding errors.

## 💡 Fun Fact: The 1/7 Mystery (2 minutes)

Calculate 1/7 as a decimal by hand using long division:

```
1 ÷ 7 = 0.142857142857...
```

Keep going for 12 decimal places - you'll see the same 6 digits (142857) repeat forever! This is called a "repeating decimal."

**Try these:**
- 1/3 = 0.333... (repeats "3")
- 1/9 = 0.111... (repeats "1")  
- 2/7 = 0.285714285714... (repeats "285714")

Each fraction has its own unique repeating pattern when converted to decimal. Some fractions (like 1/2 = 0.5) terminate, others repeat forever. This happens because of the mathematical relationship between the denominator and our base-10 number system!

***
