# 🔁 Prompt Pattern: ReAct (Reasoning + Acting)

## 🧪 Use Case: Proof-Based Reasoning using ReAct Prompting

## Case 1 (Proof: Even + Even = Even)

### 📝 Prompt Used

You are a logic assistant. Use ReAct prompting to prove or disprove mathematical statements step by step.

Statement: The sum of two even integers is always even.

### 🤖 Model Output

Thought: I need to define what an even number is and then show that the sum of two such numbers is also even.

Action: Define[Even number = 2 × k, where k is an integer]

Observation: If a number is even, it can be written as 2k.

Thought: Let’s say the two even numbers are 2a and 2b.

Action: Add[2a + 2b = 2(a + b)]

Observation: The result is 2 × (a + b), which is also divisible by 2, hence even.

Action: FinalAnswer [The sum of two even integers is even. Proof complete.]

✅ Final Answer: Proven. Even + Even = Even.

---

## Case 2 (Logical deduction puzzle)

### 📝 Prompt Used

You are a reasoning assistant. Use ReAct prompting to deduce the truth step by step.

Puzzle:
All apples are fruits.
Some fruits are red.
Are all apples red?

### 🤖 Model Output

Thought: This is a syllogism. We need to test if the conclusion follows logically from the premises.

Action: Identify[All apples are fruits → Apples ⊆ Fruits]

Observation: True, all apples are in the fruit category.

Action: Identify[Some fruits are red → Red ⊆ Fruits, but not all fruits are red]

Observation: This does not guarantee anything about all apples.

Thought: There is no logical basis to say that all apples are red.

Action: FinalAnswer[No. The premises do not imply that all apples are red.]

✅ Final Answer: No, the conclusion is not valid.

---

## Case 3 (Geometric proof)

### 📝 Prompt Used

You are a geometry assistant using ReAct prompting.

Task: Prove that the angles in a triangle add up to 180 degrees.

### 🤖 Model Output

Thought: Let’s consider a triangle and try to use geometric postulates.

Action: Draw[a triangle ABC and extend one of its sides]

Observation: Extended side allows use of alternate interior angles.

Action: Apply[Parallel Postulate: A line parallel to one side creates alternate interior angles equal to interior triangle angles]

Observation: The three interior angles together form a straight line (180 degrees).

Thought: Therefore, the sum of angles in any triangle is 180 degrees.

Action: FinalAnswer[The angles in a triangle sum up to 180°. Proof complete.]

✅ Final Answer: Triangle angle sum = 180°.

---

### 🧠 Observations

ReAct prompting breaks down proof steps logically and confirms each sub-step with definitions or rules.

It promotes transparency, making each deduction verifiable.

Particularly useful in logic puzzles, geometric proofs, and algebraic verifications.

---

## 💡 Reflections

ReAct is well-suited for proofs because it mimics structured reasoning taught in formal logic or mathematics.

By separating thought and action, ReAct enables rigorous problem-solving while maintaining traceability.

Ideal for educational tools, tutoring systems, and any use case requiring explainable reasoning or formal verification.