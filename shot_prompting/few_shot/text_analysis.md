# 🔁 Prompt Pattern: Few-Shot Prompting

## 🧪 Use Case: Text Style Transfer

Few-shot prompting helps models imitate stylistic transformations by learning from 2–3 examples in the prompt. It's ideal for creative tasks that require consistency in tone or register.

## Case 1 (Formal to Casual)

### 📝 Prompt Used

Convert the following formal sentences into casual speech.

Example 1:
Formal: I would appreciate it if you could send me the report by tomorrow.
Casual: Can you send me the report by tomorrow?

Example 2:
Formal: Kindly refrain from making noise during the presentation.
Casual: Please don’t make noise during the presentation.

Now convert:

1.Formal: It is imperative that you attend the meeting at 10 AM.

2.Formal: All board members are hereby notified about the changes in Privacy policy of the company and urged to complete the mandatory training to be deemed qualified for further operations.

3.Formal: As per the Quarter sales reports, the chains in Tokyo have been undermined by their counterparts in London.

### 🤖 Model Output

Here are the casual versions of the given formal sentences:

Formal: It is imperative that you attend the meeting at 10 AM.

Casual: You really need to be at the 10 AM meeting.

Formal: All board members are hereby notified about the changes in Privacy policy of the company and urged to complete the mandatory training to be deemed qualified for further operations.

Casual: Just a heads-up to all board members — there are updates to the company’s privacy policy, and you’ll need to finish the required training to keep things running.

Formal: As per the Quarter sales reports, the chains in Tokyo have been undermined by their counterparts in London.

Casual: According to the quarterly sales, the Tokyo branches got outperformed by the ones in London.

---

## Case 2 (Passive to Active Voice)

### 📝 Prompt Used

Convert passive sentences into active voice.

Example 1:
Passive: The book was written by the author in 1990.
Active: The author wrote the book in 1990.

Example 2:
Passive: The cake was eaten by the children.
Active: The children ate the cake.

Now convert:

1.Passive: The decision was made by the board yesterday.

2.Passive: The students found to be skipping classes, were rusticated by the Principal.

3.Passive: The Annual athletic meet was hosted by the Red group right before the final exams.

### 🤖 Model Output

Here are the active voice versions of the given passive sentences:

Passive: The decision was made by the board yesterday.

Active: The board made the decision yesterday.

Passive: The students found to be skipping classes, were rusticated by the Principal.

Active: The Principal rusticated the students who were found skipping classes.

Passive: The Annual athletic meet was hosted by the Red group right before the final exams.

Active: The Red group hosted the Annual athletic meet right before the final exams.

---

## Case 3 (Modernize Archaic Language)

### 📝 Prompt Used

Modernize the following old-fashioned English phrases.

Example 1:
Archaic: Thou shalt not lie.
Modern: You shouldn’t lie.

Example 2:
Archaic: He hath gone to the market.
Modern: He has gone to the market.

Now convert:

1.Archaic: I beseech thee to reconsider.

2.Archaic: I do delight in wandering, yet my betrothed is not fond of journeying abroad.

3.Archaic: I am taken ill; do summon the physician forthwith, I pray thee.

4.Archaic: I fear I shan’t be able to call upon thee; perchance we might convene at a later hour.

### 🤖 Model Output

Here are the modern versions of the given old-fashioned English phrases:

Archaic: I beseech thee to reconsider.

Modern: I’m asking you to please reconsider.

Archaic: I do delight in wandering, yet my betrothed is not fond of journeying abroad.

Modern: I love to travel, but my fiancé isn’t really into it.

Archaic: I am taken ill; do summon the physician forthwith, I pray thee.

Modern: I’m feeling sick—please call the doctor right away.

Archaic: I fear I shan’t be able to call upon thee; perchance we might convene at a later hour.

Modern: I don’t think I’ll be able to visit you—maybe we can meet up later.

---

### 🧠 Observations

The model learns the transformation logic from a few consistent examples.

Few-shot prompting is ideal for tasks that rely more on pattern matching and tone shifting than raw computation.

Examples act as "style templates" that steer the model.

---

## 💡 Reflections

Few-shot prompting is highly effective in style-based tasks such as rewriting, paraphrasing, or formalizing text.

By clearly showing before-and-after pairs, we reduce ambiguity and set expectations.

Works best when:

- Examples are well-chosen and aligned.

- Tasks require creative reinterpretation rather than strict logic.