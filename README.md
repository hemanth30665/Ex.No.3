# Ex.No.3 — Scenario-Based Report Development Utilizing Diverse Prompting Techniques

**NAME:** JANDA HEMANTH

**REGISTER NUMBER:** 212223030015


---

## Aim

To write prompts for four prompt engineering types — **Straightforward Prompts, Tabular Format Prompting, Preceding Question Prompting, and Missing Word Prompting** — and evaluate them using a rubric-based method; and to apply these same techniques to design an AI-powered customer service chatbot that assists with product troubleshooting, order tracking, and general inquiries in a conversational, user-friendly tone.

---

## Use Case 

**Scenario:** An AI-powered customer service chatbot for an e-commerce platform, designed to:
- Resolve **product troubleshooting** queries.
- Provide **order tracking** updates.
- Answer **general inquiries** (returns, payment, shipping policy, etc.)
- Maintain a **conversational, user-friendly tone** throughout.

All four prompt types below are applied specifically to designing and testing this chatbot.

---

## Procedure

1. Understand each of the four prompt engineering types.
2. Write example prompts of each type tailored to the chatbot design use case.
3. Record the AI-generated output for each prompt.
4. Evaluate all four techniques using a rubric across Clarity, Specificity, Usefulness for Design, and Response Quality.
5. Summarize which technique suited which part of the chatbot design process.

---

## 1. Straightforward Prompts

**Definition:** Direct, simple, single-intent prompts with no special structure — best for quick facts or short lists.

**Prompt 1:** "List three common customer issues an e-commerce chatbot should be able to handle."

**Sample Output:**
> 1. Delayed or missing order delivery.
> 2. Product not working as expected / troubleshooting help.
> 3. Refund or return status inquiries.

**Prompt 2:** "Define 'order tracking' in one sentence, the way a chatbot would explain it to a customer."

**Sample Output:**
> "Order tracking lets you check the current status and estimated delivery date of your order using your order ID or tracking number."

---

## 2. Tabular Format Prompting

**Definition:** Prompts that explicitly request a table structure — ideal for comparisons or organizing multiple related items.

**Prompt 1:** "Provide a table listing five chatbot intents for an e-commerce customer service bot, an example user query for each, and the chatbot's ideal response type."

**Sample Output:**

| Intent | Example User Query | Ideal Response Type |
|---|---|---|
| Order Tracking | "Where is my order #12345?" | Real-time status with estimated delivery date |
| Product Troubleshooting | "My headphones won't pair." | Step-by-step guided troubleshooting |
| Return/Refund | "How do I return this item?" | Policy summary + return process link |
| Payment Issue | "My payment failed twice." | Reassurance + escalation to payment support |
| General Inquiry | "What are your store hours?" | Direct factual answer |

**Prompt 2:** "Compare rule-based chatbots and LLM-based chatbots in a table across cost, flexibility, and accuracy for customer service use."

**Sample Output:**

| Aspect | Rule-Based Chatbot | LLM-Based Chatbot |
|---|---|---|
| Cost | Lower ongoing cost, cheaper to build | Higher API/compute cost |
| Flexibility | Limited to predefined intents/flows | Handles unexpected/complex phrasing well |
| Accuracy | High for narrow, well-defined tasks | High for broad understanding, needs guardrails for factual accuracy |

---

## 3. Preceding Question Prompting

**Definition:** A prompt structured as a lead-in question followed by a request to explain — useful for generating reasoned, explanatory content rather than a flat list.

**Prompt 1:** "Why do customers abandon chat conversations with a bot? Explain how a chatbot's tone and response time affect user satisfaction."

**Sample Output:**
> Customers often abandon chatbot conversations when responses feel robotic, repetitive, or too slow. A conversational, empathetic tone reduces frustration by making the interaction feel human-like, while fast response time keeps momentum in the conversation — even a few seconds of delay can cause users to disengage, especially for time-sensitive queries like order tracking.

**Prompt 2:** "How does a chatbot resolve an order tracking query? Describe the step-by-step process from user query to order status response."

**Sample Output:**
> 1. The chatbot detects the "order tracking" intent from the user's message.
> 2. It requests the order ID or associates the query with the logged-in user's account.
> 3. It queries the order management system/API for the current status.
> 4. It formats the raw status data into a friendly, conversational reply.
> 5. It offers a follow-up action, such as "Would you like delivery notifications?"

---

## 4. Missing Word Prompting

**Definition:** A fill-in-the-blank style prompt that constrains the AI to produce a specific, targeted piece of information.

**Prompt 1:** "When a customer asks about a delayed order, the chatbot should first ____ before providing an update."

**Sample Output:**
> "...acknowledge the inconvenience and apologize for the delay..."

**Prompt 2:** "A good troubleshooting chatbot response should be ____, ____, and ____."

**Sample Output:**
> "...clear, concise, and empathetic."

---

## Evaluation (Rubric-Based Method)

Each technique was scored 1–5 on four criteria, based on its usefulness specifically for **chatbot design work**.

| Prompt Type | Clarity | Specificity | Usefulness for Design | Response Quality | Total (/20) |
|---|---|---|---|---|---|
| Straightforward Prompts | 5 | 3 | 3 | 4 | 15 |
| Tabular Format Prompting | 5 | 5 | 5 | 5 | 20 |
| Preceding Question Prompting | 4 | 4 | 4 | 5 | 17 |
| Missing Word Prompting | 4 | 5 | 3 | 3 | 15 |

### Observations

- **Tabular Format Prompting** scored highest overall — organizing chatbot intents, example queries, and response types into a table was directly usable as a design artifact (an intent-response map), not just descriptive text.
- **Preceding Question Prompting** was most useful for understanding *why* certain chatbot behaviors matter (tone, response time) and for documenting a *process* (the order-tracking resolution flow) — valuable for writing design rationale and technical documentation.
- **Straightforward Prompts** were fast and clear but too shallow to drive actual design decisions on their own — useful mainly for quick fact-checks or brainstorming seed ideas.
- **Missing Word Prompting** was effective for extracting very specific, constrained answers (e.g., the three qualities of a good response) but too narrow to use for open-ended design exploration — best used to pin down a specific detail once the broader design is already in place.

---

## Conclusion

Applying Straightforward, Tabular Format, Preceding Question, and Missing Word prompting to the design of an AI-powered customer service chatbot showed that different prompt types serve distinct roles in a real design workflow: Tabular Format Prompting was best for organizing structured design artifacts (intent-response tables, comparisons), Preceding Question Prompting was best for generating design rationale and process explanations, Straightforward Prompts were best for quick fact retrieval, and Missing Word Prompting was best for pinning down specific, constrained details. Using the right prompt type for the right sub-task produced more useful, directly applicable outputs than relying on a single prompting style throughout.

---

## Result

The prompts for all four prompt engineering types — Straightforward, Tabular Format, Preceding Question, and Missing Word Prompting — were written, executed, and evaluated successfully for the AI-powered customer service chatbot use case (product troubleshooting, order tracking, and general inquiries), with Tabular Format Prompting scoring highest overall for chatbot design work under the rubric evaluation used.
