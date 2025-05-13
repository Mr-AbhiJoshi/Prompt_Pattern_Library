# 🔁 Prompt Pattern: Chain of Thought (CoT)

## 🧪 Use Case: Solving Coding Problems

## Case 1 (Debugging a Python function)

### 📝 Prompt Used

You are a helpful assistant that solves coding problems step by step.

Question: The following Python function is intended to return the sum of all even numbers in a list, but it’s returning 0. Fix it.

```python
def sum_even_numbers(lst):
    for num in lst:
        if num % 2 == 0:
            total = 0
            total += num
    return total

print(sum_even_numbers([2, 4, 6]))
```

### 🤖 Model Output

Let's debug the function step by step:

Step 1: Look at where `total = 0` is initialized. It’s inside the loop, so it resets to 0 on each iteration. That’s a bug.

Step 2: `total` should be initialized **before** the loop so it can accumulate values.

Step 3: Rewrite the function correctly:

```python
def sum_even_numbers(lst):
    total = 0
    for num in lst:
        if num % 2 == 0:
            total += num
    return total
```

Step 4: Test the fixed function:
```python
print(sum_even_numbers([2, 4, 6]))
```

✅ Final Answer: The corrected function returns the expected output 12.

---

## Case 2 (Algorithm design – Finding the maximum product of two numbers in a list)

### 📝 Prompt Used

You are an assistant that solves programming problems by reasoning through them step by step.

Question: Given a list of integers, return the maximum product of any two numbers. Explain your reasoning.

Input: [3, 5, -2, 9, -10]

### 🤖 Model Output

Let's approach this step by step:

Step 1: We need the two numbers whose product is the highest.

Step 2: That could either be:

the two largest positive numbers, or

the two smallest (most negative) numbers, since multiplying two negatives gives a positive.

Step 3: Sort the list: [-10, -2, 3, 5, 9]

Step 4: Compute products:

Product of two largest positives: 9 × 5 = 45

Product of two smallest negatives: -10 × -2 = 20

Step 5: The larger of the two products is 45.

✅ Final Answer: 45

---

## Case 3 (Understanding recursion in a factorial function)

### 📝 Prompt Used

You are a programming tutor that explains code step by step.

Question: How does the following recursive factorial function work for input 4?

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n-1)

print(factorial(4))
```

### 🤖 Model Output

Let’s evaluate `factorial(4)` step by step:

Step 1: `factorial(4)`  
→ returns `4 * factorial(3)`

Step 2: `factorial(3)`  
→ returns `3 * factorial(2)`

Step 3: `factorial(2)`  
→ returns `2 * factorial(1)`

Step 4: `factorial(1)`  
→ returns `1 * factorial(0)`

Step 5: `factorial(0)`  
→ base case hit, returns `1`

Now we resolve the calls in reverse:

- `factorial(1)` = 1 * 1 = 1  
- `factorial(2)` = 2 * 1 = 2  
- `factorial(3)` = 3 * 2 = 6  
- `factorial(4)` = 4 * 6 = 24

✅ Final Answer: 24

---

### 🧠 Observations

The Chain of Thought prompt guided the model through each coding problem with clarity.

It helped isolate issues (like logic bugs or design flaws) by breaking them down step by step.

This structure made it easier to understand why an error occurred and how to fix it.

CoT proved effective not only for reasoning but also for debugging and algorithm design.

---

## 💡 Reflections

Chain of Thought prompting is highly effective for solving programming problems.

It mirrors how developers approach tasks—through decomposition, logical reasoning, and stepwise correction.

Especially helpful in scenarios like debugging, understanding recursion, and analyzing edge cases.

Combining CoT with specific instructions like “analyze this bug” or “design an algorithm step by step” can yield even better results.