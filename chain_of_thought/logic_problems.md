# 🔁 Prompt Pattern: Chain of Thought (CoT)

## 🧪 Use Case: Solving Logic Problems

## Case 1 (Truth-teller and liar problem)

### 📝 Prompt Used

You are a reasoning assistant that solves logic puzzles step by step.

Question: You meet two people: Alice and Bob. One of them always tells the truth, the other always lies.

Alice says, "Bob is the liar."  
Bob says, "We are both liars."

Who is the truth-teller?

### 🤖 Model Output

Let’s reason through this:

Step 1: Bob says, “We are both liars.” If Bob were telling the truth, then they would both be liars. But a truth-teller can’t claim to be a liar — that’s a contradiction.

Step 2: So Bob must be lying.

Step 3: That means his statement "We are both liars" is false. Therefore, it’s not true that both are liars → which implies one of them is telling the truth.

Step 4: Alice says, “Bob is the liar.” Since Bob is the liar, Alice must be telling the truth.

✅ Final Answer: Alice is the truth-teller.

---

## Case 2 (Logical deduction – identifying the criminal)

### 📝 Prompt Used

You are a logic puzzle solver. Work step by step.

Question: Three suspects — Anna, Brian, and Clara — are questioned.

- Anna says: “I didn’t do it. Brian did it.”
- Brian says: “I didn’t do it.”
- Clara says: “Anna did it.”

Only one person is telling the truth. Who committed the crime?

### 🤖 Model Output

Let’s test each suspect as the possible truth-teller.

Option 1: Anna is telling the truth

→ “I didn’t do it. Brian did it.”

→ That means Brian is guilty.

→ Brian says “I didn’t do it” → this would be a lie.

→ Clara says “Anna did it” → also a lie.

✅ This setup works. Only Anna is telling the truth.

Option 2: Brian is telling the truth

→ “I didn’t do it”

→ Then Anna is lying → she did it or Brian didn’t do it.

→ Clara says Anna did it → would be true, but now two people (Brian and Clara) are telling the truth → contradiction.

Option 3: Clara is telling the truth

→ “Anna did it”
→ Then Anna is lying → she did it or Brian didn’t.

→ Brian says “I didn’t do it” → true → again two people are truthful → contradiction.

✅ Final Answer: Brian committed the crime. Anna is the only one telling the truth.

---

## **Important** Case 3 (Seating arrangement logic)

#### Note: In this example, we will see, how sometimes model just starts to hallucinate and provide contradictory answers.

### 📝 Prompt Attempt 1

You are a step-by-step logic assistant.

Question: Four friends (Alex, Blake, Chris, Dana) are sitting in a row.

- Alex is not at either end.
- Dana is to the right of Chris.
- Blake is not next to Dana.

In what order are they sitting (left to right)?

### 🤖 Model Output

Let’s go step by step.

Step 1: There are 4 positions: [ _ , _ , _ , _ ]

Step 2: "Alex is not at either end" → so Alex is in position 2 or 3.

Step 3: "Dana is to the right of Chris" → Dana must be seated after Chris (i.e., higher index).

Step 4: "Blake is not next to Dana" → Blake can't be immediately adjacent to Dana.

Let’s try placing Chris at position 1:

Chris at 1 → Dana must be at 2, 3, or 4 (right of Chris)

Try Dana at 3

→ Alex can go at 2 (valid)

→ That leaves Blake at 4

But now: Dana (3), Blake (4) → they are next to each other → ❌ violates "Blake not next to Dana"

Try Dana at position 4: Chris at 1, Dana at 4

Alex at 2 → valid

Blake at 3 → now Blake is next to Dana → ❌ violates constraint again.

Try Dana at 3: Chris at 1, Dana at 3, Alex at 2, Blake at 4 → Dana and Blake again adjacent → ❌

Try Dana at 2:

Chris at 1

Dana at 2 → Blake cannot be at 1 or 3 → stuck.

Now try Chris at position 2, Dana at 3:

Chris at 2

Dana at 3 → satisfies “Dana is to the right of Chris”

Alex must be at 2 or 3 → both taken
→ So Alex goes at position 4 → ❌ violates "not at ends"

Eventually, try:

Chris at 1

Alex at 2

Dana at 4

Blake at 3 → Blake and Dana are not adjacent → ✅ valid

✅ Final Answer: [Chris, Alex, Blake, Dana]

#### See, how even though we had mentioned Blake is not next to Dana, the model has chosen to ignore it, and just provide us with a made-up answer. Now, to correct it, we will ask it to explain it's reasoning for steps.

### 📝 Prompt Attempt 2

Try solving this problem again. Explain your reasoning at each step.

You are a step-by-step logic assistant.

Question: Four friends (Alex, Blake, Chris, Dana) are sitting in a row.

- Alex is not at either end.
- Dana is to the right of Chris.
- Blake is not next to Dana.

In what order are they sitting (left to right)?

### 🤖 Model Output

🧩 Problem: We have 4 friends: Alex, Blake, Chris, Dana. They are sitting in a row of 4 seats (left to right), and we are given three constraints:

Alex is not at either end. → So Alex can only be in position 2 or 3.

Dana is to the right of Chris. → Dana must sit in a higher-numbered seat than Chris.

Blake is not next to Dana. → They cannot be adjacent.

✅ Step-by-step Reasoning

Let’s represent the 4 positions as:

[ _, _, _, _ ] → Positions 1, 2, 3, 4 (left to right)

Let’s now iterate through valid placements of Alex (since constraint #1 limits her positions).

🔍 Try placing Alex at position 2:

Current: [ _, Alex, _, _ ]

Remaining people: Blake, Chris, Dana

Let’s now try assigning Chris and Dana in a way that satisfies “Dana is to the right of Chris”.

Try: Chris at 1, Dana at 3

Now we have: [Chris, Alex, Dana, _]

Remaining: Blake → must go at position 4

Final: [Chris, Alex, Dana, Blake]

Now validate all constraints:

✅ Alex is not at either end → position 2 ✅

✅ Dana is to the right of Chris (Chris at 1, Dana at 3) ✅

❌ Blake is next to Dana (positions 3 and 4) → violates constraint

Try a different configuration.

🔁 Keep Alex at position 2, but try Dana at 4 and Chris at 1:

Now: [Chris, Alex, _, Dana]

Remaining: Blake → only position 3

Final: [Chris, Alex, Blake, Dana]

Check constraints:

✅ Alex not at either end → position 2 ✅

✅ Dana (4) is to the right of Chris (1) ✅

✅ Blake (3) is not next to Dana (4) ❌ → actually, they are adjacent → violates constraint

🔁 Try Alex at position 3 instead:

Current: [ _, _, Alex, _ ]

Available: 1, 2, 4

Try placing Chris at 1, Dana at 2 → Dana is not to the right of Chris → ❌

Try Chris at 1, Dana at 4:

Now: [Chris, _, Alex, Dana]

Remaining: Blake → only position 2

Final: [Chris, Blake, Alex, Dana]

Check:

✅ Alex not at ends → position 3 ✅

✅ Dana (4) is to the right of Chris (1) ✅

✅ Blake (2) is not next to Dana (4) → Dana is at 4, Blake at 2 → not adjacent ✅

✅ All constraints satisfied!

🧾 Final Answer: [Chris, Blake, Alex, Dana]

---

### 🧠 Observations

Chain of Thought prompting helped unpack complex conditions and conflicting constraints.

The model could simulate multiple scenarios, reject invalid ones, and converge on the correct solution.

This systematic approach avoids guessing and mirrors how a human would reason through logic puzzles.

---

## 💡 Reflections

CoT is a powerful tool for logic-based problems involving deduction, elimination, and simulation of outcomes.

It encourages hypothesis testing and constraint satisfaction—core strategies in logical reasoning.

When faced with puzzles, conflicting statements, or multi-step inferences, CoT helps the model “think out loud.”

Combining CoT with a directive like “evaluate all possibilities” or “eliminate contradictions” can yield highly reliable results.