# 🔁 Prompt Pattern: ReAct (Reasoning + Acting)

## 🧪 Use Case: Interactive Question Answering with Tools or Simulated Actions

## Case 1 (Movie selection from a database)

### 📝 Prompt Used

You are an assistant who selects the best movie using ReAct prompting.
You must think aloud, then simulate actions such as Search[], Filter[], and FinalAnswer[].

Task: Find a science fiction movie from the 2010s with high ratings and strong female leads.

### 🤖 Model Output

Thought: I need to find science fiction movies from the 2010s, then filter for high ratings and strong female leads.

Action: Search[science fiction movies from 2010 to 2019]

Observation: Found a list including Arrival (2016), Interstellar (2014), Ex Machina (2015), The Martian (2015)

Thought: Now I’ll filter for high ratings (e.g., IMDb > 7.5)

Action: Filter[movies with IMDb > 7.5]

Observation: All listed movies meet the criteria.

Thought: Now check for strong female leads.

Action: Filter[movies with central female characters]

Observation:

Arrival stars Amy Adams as a linguist who deciphers alien language

Ex Machina features Alicia Vikander as an AI

Interstellar includes Anne Hathaway, but she is not the central lead

The Martian stars Matt Damon

Thought: Arrival and Ex Machina are the best fits.

Action: FinalAnswer[Arrival (2016)]

✅ Final Answer: Arrival (2016)

---

## Case 2 (Troubleshooting a printer issue)

### 📝 Prompt Used

You are a support assistant that uses ReAct prompting to diagnose and resolve issues.

Task: A user says their wireless printer is not printing, even though it’s connected to Wi-Fi.

### 🤖 Model Output

Thought: I should check if the printer is recognized by the computer.

Action: AskUser[Can your computer detect the printer in the device list?]

Observation: Yes, it shows up as "HP Envy 4520" in the device list.

Thought: Next, check the print queue or if any errors show.

Action: AskUser[Are there any documents stuck in the print queue or error messages?]

Observation: Yes, there's a job stuck with an error "offline printer."

Thought: The printer might be in sleep mode or needs to be reset.

Action: Suggest[Power cycle the printer and try printing again.]

Observation: User restarted the printer and the print job succeeded.

Action: FinalAnswer[Issue resolved by power cycling. Printer was stuck in sleep/offline mode.]

✅ Final Answer: Printer was offline. Restarting it resolved the issue.

---

## Case 3 (Solving a text-based puzzle)

### 📝 Prompt Used

You are a reasoning detective assistant. Use ReAct prompting to solve the mystery step by step.

Task: Solve the mystery from the clues.

Clues:
1. The painting was stolen at night.
2. Only two people had access: the butler and the maid.
3. The maid says she was preparing breakfast at the time.
4. The butler says he was fixing a fuse due to a power cut at 10 PM.
5. The CCTV confirms the power cut occurred at 10 PM.

### 🤖 Model Output

Thought: Let's cross-reference the statements with the clue about time.

Action: Verify[When was the painting stolen?]

Observation: It was stolen at 10 PM during the power outage.

Thought: The maid claims she was making breakfast — that doesn’t add up.

Action: Analyze[Does preparing breakfast at 10 PM make sense?]

Observation: No. Breakfast preparation typically happens in the morning.

Thought: The maid's alibi is suspicious.

Action: FinalAnswer[The maid is lying and is the likely thief.]

✅ Final Answer: The maid is the thief. Her alibi contradicts the timeline.

---

### 🧠 Observations

ReAct encourages deliberate, modular thinking: the model reasons, acts, observes, and loops.

It excels at problems involving external information gathering, stateful interactions, or multi-step decision-making.

The structure mimics how real-world agents behave.

---

## 💡 Reflections

ReAct prompting is ideal for interactive tasks that require both thinking and doing.

It offers transparency at each step: how the model reasons, what actions it takes, and what it learns from them.

Useful in areas like customer support, research assistants, and puzzle solving — anywhere that involves incremental deduction or tool use.

Combining ReAct with retrieval tools, calculators, or simulated APIs unlocks even more practical use cases.