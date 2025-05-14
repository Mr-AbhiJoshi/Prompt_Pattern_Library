# 🔁 Prompt Pattern: Zero-Shot Prompting

## 🧪 Use Case: Reasoning-Based Problem Solving

With carefully worded instructions, zero-shot prompting can solve logical and numeric problems directly — no step-by-step examples needed. Works best when the task is commonly seen or has a natural reasoning path.

## Case 1 (Riddle Solving)

### 📝 Prompt Used

Solve the riddle:  
I speak without a mouth and hear without ears. I have no body, but I come alive with the wind. What am I?

### 🤖 Model Output

An echo.

---

## Case 2 (Math Word Problem)

### 📝 Prompt Used

A train travels 60 miles per hour for 3 hours. How far does it travel in total?

### 🤖 Model Output

The train travels 180 miles in total.

---

## Case 3 (Rewrite as a Poem)

### 📝 Prompt Used

If all roses are flowers, and some flowers fade quickly, can we conclude that some roses fade quickly?

### 🤖 Model Output

No, because the statement only says some flowers fade quickly, not that roses specifically do.

---

### 🧠 Observations

Zero-shot reasoning works well when the logic is common-sense, deductive, or elementary math.

The model often uses internal heuristics learned during pretraining to infer answers.

Still, complex reasoning can benefit from chain-of-thought or few-shot prompting.

---

## 💡 Reflections

Use zero-shot for reasoning problems when:

- The logic is direct and doesn’t require deep chains of steps.

- You value speed and minimal setup over traceable reasoning.

- You're testing the model’s ability to generalize without examples.

It’s a quick and effective way to test knowledge, logic, or perform lightweight problem solving.