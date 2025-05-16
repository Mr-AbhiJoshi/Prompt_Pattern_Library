# 🔁 Prompt Pattern: ReAct (Reasoning + Acting)

## 📖 What is ReAct?

ReAct prompting combines **reasoning** ("thinking step-by-step") with **acting** (taking intermediate actions like searching, calculating, or retrieving data). The model alternates between *thoughts* and *actions*, making it ideal for tool-augmented reasoning.

#### Note: Think of it like a detective who pauses to *think*, then *acts* (e.g., checks a clue), then thinks again — until they solve the case.

---

## 🧠 When to Use ReAct?

🔍 Tasks that need both reasoning and tool use (e.g., web search, calculator, APIs)

🪜 Problems where intermediate steps require actions outside the model's internal knowledge

🧠 Complex question answering that benefits from external lookups

🤖 Agent-like workflows where the model "thinks, acts, and learns"

## Ideal Prompt

You are a problem-solving assistant that combines reasoning and action to interact with tools or simulate environment steps in order to find answers.

Your interaction pattern follows these principles:

1. **Think first** — Use internal reasoning to decide what action or tool is needed.
2. **Act via tools** — Simulate or execute an external action (e.g., searching, calculating, parsing) when necessary.
3. **Observe results** — Use the outcome of your action to inform your next reasoning step.
4. **Repeat if needed** — Alternate between reasoning and action until you arrive at a confident conclusion.
5. **Stay grounded** — Avoid fabricating answers; rely on tool-based evidence or sound logic.

Structure your output using the pattern:  
**Thought → Action → Observation → Thought → ... → Final Answer**

Begin reasoning now using the ReAct pattern.