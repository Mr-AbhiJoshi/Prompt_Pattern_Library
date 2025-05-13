# 🔁 Prompt Pattern: Chain of Thought (CoT)

## 🧪 Use Case: Solving Word Problems

---

## Case 1 (Problem derived from sentences)

### 📝 Prompt Used

```text
You are a smart assistant that solves problems by reasoning step by step.

Question: Sarah gave 3 pencils to her friend and then bought 5 more. Her friend again asked for 6 pencils, which Sarah gave, and then got 4 more from her teacher. At the end, Sarah had 10 pencils. How many pencils did she have at starting?
```

### 🤖 Model Output

Let’s break it down step by step by letting x be the number of pencils Sarah had at the beginning.

Started with: x pencils

Gave 3 to friend: x - 3

Bought 5 more: (x - 3) + 5 = x + 2

Gave 6 to friend: (x + 2) - 6 = x - 4

Got 4 from teacher: (x - 4) + 4 = x

So she ends up with x pencils, and the question says she had 10 pencils at the end. Thus, She had 10 pencils at the start.

---

## Case 2 (Simple arithmetic problem)

### 📝 Prompt Used

```text
You are a smart assistant that solves problems by reasoning step by step.

Question: Solve (4*6)^2/8+21x9
```

### 🤖 Model Output

Let's solve the expression step by step:

Step 1: Multiply inside parentheses: 4×6=24

Step 2: Square the result: 24^2=576

Step 3: Divide by 8: 576/8=72

Step 4: Multiply 21 × 9: 21×9=189

Step 5: Add the two parts: 72+189=261
​
✅ Final Answer: 261

---

## Case 3

### 📝 Prompt Used (Reasoning based problem)

```text
You are a smart assistant that solves problems by reasoning step by step.

Question: Ramesh Sharma is the father of Neha and Suresh. Neha is married to Rajiv Mehta, and they have a daughter named Diya. Suresh is married to Anjali, and they have a son named Aarav. Anjali refers to Ramesh Sharma as "Papa ji," and Ramesh’s wife, Sunita Sharma, is Aarav’s grandmother. Rajiv Mehta's younger brother, Sameer, is unmarried and lives with Rajiv’s family. Diya calls Sameer “Chachu” (paternal uncle). Aarav, meanwhile, visits Rajiv’s home during festivals and touches the feet of both Rajiv and Neha as a mark of respect. Neha is often referred to as "Bua" (father’s sister) by Aarav. Based on this information, What is the exact relationship between Aarav and Diya?
```

### 🤖 Model Output

To determine the exact relationship between Aarav and Diya, let's analyze the family structure step by step:

1. Core Family Members
Ramesh Sharma (father of Neha and Suresh) → Married to Sunita Sharma
Their children: Neha (daughter), Suresh (son)

2. Neha’s Family
Neha is married to Rajiv Mehta. They have a daughter named Diya.
So: Diya is the daughter of Neha and Rajiv

3. Suresh’s Family
Suresh is married to Anjali. They have a son named Aarav.
So: Aarav is the son of Suresh and Anjali

4. Relationship between Diya and Aarav
Neha and Suresh are siblings (brother and sister)
Diya is Neha’s daughter, meanwhile Aarav is Suresh’s son
So:
👉 Diya’s mother (Neha) is Aarav’s Bua (father’s sister)
👉 Aarav’s father (Suresh) is Diya’s Mama (mother’s brother)

✅ Conclusion
Diya and Aarav are first cousins — specifically, maternal cousin for Diya and paternal cousin for Aarav. They are cousins (first cousins).
---

### 🧠 Observations

The Chain of Thought prompt encouraged structured, transparent thinking.

The model correctly performed each sub-step of the problem.

The structure improves traceability and debuggability of answers.

---

## 💡 Reflections

CoT is very useful for simple arithmetic and reasoning-based problems.

It can be combined with additional instructions like “explain your answer” or “show all steps” for even better performance.

Works especially well when tasks resemble how humans think logically.