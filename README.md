# Ex. No. 3 — Scenario-Based Report Development Utilizing Diverse Prompting Techniques



## Aim

To write prompts for the following prompt engineering types and evaluate them:

1. Straightforward Prompts
2. Tabular Format Prompting
3. Preceding Question Prompting
4. Missing Word Prompting

## Problem Statement / Explanation

Prompt engineering is the practice of designing inputs to a generative AI/LLM system so that it produces the most accurate, relevant, and useful output. Different prompting styles suit different goals — a direct instruction works well for simple factual recall, a tabular prompt is ideal when structured comparison is needed, a preceding-question prompt frames context before asking for an explanation, and a missing-word (cloze-style) prompt tests or elicits precise, targeted recall. This report takes one use case — **explaining core science and technology concepts to a learner** — and demonstrates it across all four prompt types, evaluating the output quality of each.

## Algorithm / Procedure

**Step 1: Straightforward Prompts** Give the model a direct, unambiguous instruction with no additional framing, and evaluate the directness and conciseness of the response.

**Step 2: Tabular Format Prompting** Instruct the model to structure its output as a table with defined columns, and evaluate clarity and ease of comparison.

**Step 3: Preceding Question Prompting** Pose a question first, followed by a request for explanation, to give the model explicit context before the detailed answer, and evaluate depth and relevance.

**Step 4: Missing Word Prompting** Give the model a sentence with a blank ("___") and ask it to complete it, and evaluate factual accuracy and precision.

**Step 5: Evaluation** Compare outputs from all four types against the criteria: *clarity, structure, accuracy, and usefulness*, and record observations.

---

## 1. Straightforward Prompts

**Prompt A:** "Define blockchain in one sentence."
**Generated Output:** Blockchain is a distributed digital ledger that records transactions across many computers so that entries cannot be altered retroactively without changing all later records.

**Prompt B:** "List three advantages of solar energy."
**Generated Output:**
1. Renewable and abundant, since sunlight is naturally replenished.
2. Produces no direct emissions during electricity generation.
3. Reduces long-term electricity bills once panels are installed.

**Evaluation:** Straightforward prompts produce quick, concise, directly usable answers. Best suited for simple fact retrieval or short lists, but they offer little structure for comparing multiple attributes at once.

---

## 2. Tabular Format Prompting

**Prompt A:** "Compare and contrast HTTP and HTTPS in a table."

**Generated Output:**

| Feature | HTTP | HTTPS |
|---|---|---|
| Full form | HyperText Transfer Protocol | HTTP Secure |
| Security | Data sent in plain text | Data encrypted using SSL/TLS |
| Port used | 80 | 443 |
| Speed | Slightly faster | Marginally slower due to encryption |
| Use case | Non-sensitive browsing | Login pages, payments, sensitive data |

**Prompt B:** "Provide a table listing four types of computer memory, their speed, and one use case each."

**Generated Output:**

| Memory Type | Speed | Use Case |
|---|---|---|
| Cache | Fastest | Storing frequently used CPU data |
| RAM | Very fast | Running active programs |
| SSD | Fast | Primary storage in modern laptops |
| HDD | Slow | Bulk, low-cost long-term storage |

**Evaluation:** Tabular prompting excels when the goal is side-by-side comparison of multiple items across shared attributes. It significantly improves readability over prose for multi-point comparisons but is unnecessary for single-fact answers.

---

## 3. Preceding Question Prompting

**Prompt A:** "Why is data privacy a growing concern? Explain how anonymization protects user data."
**Generated Output:** Data privacy is a growing concern because companies collect vast amounts of personal information, and breaches or misuse can lead to identity theft, financial loss, or surveillance. Anonymization protects user data by removing or altering identifying details — such as names or ID numbers — so that individuals cannot be traced back from the dataset, allowing organizations to analyze data patterns while reducing the risk of exposing personal identities.

**Prompt B:** "How do satellites stay in orbit? Describe the balance of forces involved."
**Generated Output:** Satellites stay in orbit because of a balance between two forces: gravity, which continuously pulls the satellite toward Earth, and its forward velocity, which pushes it in a straight line. Because the satellite is moving fast enough sideways, it keeps "falling" toward Earth at the same rate the Earth's surface curves away beneath it, resulting in a stable circular or elliptical path around the planet.

**Evaluation:** Framing a question before requesting an explanation guides the model toward a more contextual, motivated response — it explains *why* something matters before *how* it works, producing richer, more pedagogically structured answers than a bare instruction.

---

## 4. Missing Word Prompting

**Prompt A:** "The powerhouse of the cell is the ___."
**Generated Output:** The powerhouse of the cell is the **mitochondria**.

**Prompt B:** "In networking, an IP address that stays the same is called a ___ IP."
**Generated Output:** In networking, an IP address that stays the same is called a **static** IP.

**Evaluation:** Missing-word (cloze) prompting is highly effective for testing or eliciting precise factual recall with minimal output — ideal for quizzes, flashcards, or verifying a model's grasp of a specific fact. It is not suited to open-ended or explanatory tasks.

---

## Comparative Summary

| Prompt Type | Best For | Output Style | Limitation |
|---|---|---|---|
| Straightforward Prompts | Quick facts, short lists | Concise, direct | Limited structure for comparisons |
| Tabular Format Prompting | Multi-attribute comparisons | Structured, scannable | Overkill for single facts |
| Preceding Question Prompting | Contextual explanations | Detailed, motivated | Longer, less concise |
| Missing Word Prompting | Precise factual recall | Minimal, targeted | Not suited for explanations |

## Conclusion

Each prompting technique serves a distinct purpose and produces a different kind of output. Straightforward prompts work best for quick facts, tabular prompting suits multi-point comparisons, preceding-question prompting produces deeper contextual explanations, and missing-word prompting is ideal for testing precise recall. Choosing the right prompt type depends on the task's goal — brevity, comparison, depth, or precision.
