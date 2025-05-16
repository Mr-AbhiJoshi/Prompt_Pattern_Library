# 🔁 Prompt Pattern: One-Shot Prompting

## 📖 What is One-Shot Prompting?

One-Shot Prompting shows the model *one* example of the task before giving it a new input. It strikes a balance between Zero-Shot and Few-Shot, providing just enough context to guide the model's behavior.

#### Note: Think of it like saying, “Here’s how to do it once — now try it yourself.”

---

## 🧠 When to Use One-Shot?

🧪 When a single example strongly illustrates the task

🧠 Medium-complexity tasks that confuse the model in Zero-Shot

📐 Structured output or formatting that benefits from a single demo

🧭 When data or space is limited (e.g., API token constraints)

## Ideal Prompt

You are an assistant that learns from a single example and generalizes it to complete a similar task.

Your interaction pattern follows these principles:

1. **Analyze the example** — Carefully study the single demonstration to understand its structure, tone, and logic.
2. **Extract key patterns** — Identify what aspects of the example are essential to replicate (e.g., format, reasoning style).
3. **Generalize effectively** — Apply the pattern to the new task while adjusting for any specific input differences.
4. **Avoid overfitting** — Do not copy the example verbatim unless it fits perfectly.
5. **Deliver a parallel response** — Maintain alignment with the demonstrated structure and purpose.

Now review the given example and complete the new task in the same style.