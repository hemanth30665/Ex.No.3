## Name: Janda Hemanth
## Reg No: 212223030015

---

# Ex. No: 3
# Date:03-08-2026

# Scenario-Based Report Development Utilizing Diverse Prompting Techniques
### (Straightforward Prompts, Tabular Format Prompting, Missing Word Prompting, Preceding Question Prompting)

---

# Aim
To write prompts for the following prompt engineering types and evaluate them using a chosen scenario/use case:
1. Straightforward Prompts
2. Tabular Format Prompting
3. Preceding Question Prompting
4. Missing Word Prompting

---

# Problem Statement
Prompt Engineering is the practice of designing effective inputs (prompts) to guide a Large Language Model (LLM) toward producing accurate, relevant, and well-structured outputs. Different prompting styles influence how the model interprets a request and structures its response. This experiment explores four fundamental prompt types — straightforward, tabular, preceding-question, and missing-word — and applies them to a real-world use case to compare their effectiveness in eliciting clear, useful, and well-organized information from an AI model.

---

# Use Case (Reference: Unit 5 – Real-World Application of Prompt Engineering)
**Chosen Use Case: AI-Assisted Learning of Renewable Energy and Environmental Science Concepts**

This use case involves a student using an AI assistant to learn foundational science concepts — such as electricity types, environmental issues, and biological processes — for exam preparation and general understanding. The four prompt types from Unit 2 are applied to this educational use case to demonstrate how different prompting strategies retrieve and structure the same underlying knowledge domain in different ways.

---

# Algorithm / Procedure

### Step 1: Straightforward Prompts
Direct, unambiguous instructions are given to the model, requesting a specific, concise piece of information without additional structure or context.

**Prompt 1:** "Define photosynthesis in one sentence."
**Prompt 2:** "List three advantages of electric vehicles."

**Generated Output:**
| Prompt | AI Response |
|---|---|
| Define photosynthesis in one sentence. | Photosynthesis is the process by which green plants use sunlight, water, and carbon dioxide to produce glucose and oxygen. |
| List three advantages of electric vehicles. | 1. Zero tailpipe emissions, reducing air pollution. 2. Lower running costs due to cheaper electricity vs. fuel. 3. Reduced dependency on fossil fuels. |

---

### Step 2: Tabular Format Prompting
The model is explicitly instructed to organize its response into a table, useful for comparisons or structured multi-attribute data.

**Prompt 1:** "Compare and contrast AC and DC current in a table."
**Prompt 2:** "Provide a table listing five programming languages, their paradigms, and one use case each."

**Generated Output (Prompt 1):**

| Feature | AC (Alternating Current) | DC (Direct Current) |
|---|---|---|
| Direction of flow | Reverses periodically | Flows in one direction |
| Source | Power plants, generators | Batteries, solar cells |
| Transmission | Efficient over long distances | Efficient over short distances |
| Common use | Household electricity | Electronic devices, batteries |

**Generated Output (Prompt 2):**

| Language | Paradigm | Use Case |
|---|---|---|
| Python | Multi-paradigm (OOP, procedural) | Data science and AI |
| Java | Object-oriented | Enterprise applications |
| JavaScript | Event-driven, functional | Web development |
| Haskell | Functional | Academic/research computing |
| C | Procedural | Systems/embedded programming |

---

### Step 3: Preceding Question Prompting
A guiding question precedes the main instruction, priming the model with context before asking it to elaborate — often producing richer, more explanatory answers.

**Prompt 1:** "Why is climate change a global concern? Explain how greenhouse gases contribute to global warming."
**Prompt 2:** "How do vaccines work? Describe the process of immunization in simple terms."

**Generated Output:**

*Prompt 1 Response:*
Climate change is a global concern because rising temperatures disrupt ecosystems, agriculture, sea levels, and weather patterns worldwide, affecting every country regardless of its contribution to emissions. Greenhouse gases such as carbon dioxide and methane trap heat in the Earth's atmosphere by absorbing infrared radiation that would otherwise escape into space, causing a gradual warming effect known as the greenhouse effect.

*Prompt 2 Response:*
Vaccines work by training the immune system to recognize and fight specific pathogens without causing the actual disease. Immunization introduces a weakened, inactivated, or partial form of a pathogen (or genetic instructions to build part of it) into the body, prompting the immune system to produce antibodies. If the real pathogen is encountered later, the immune system can respond quickly and effectively, preventing illness.

---

### Step 4: Missing Word Prompting
A sentence with a blank is provided, and the model completes it — testing recall of specific facts within a fixed context.

**Prompt 1:** "The capital of France is ____."
**Prompt 2:** "In photosynthesis, plants absorb sunlight to produce ____."

**Generated Output:**
| Prompt | Completed Response |
|---|---|
| The capital of France is ____. | The capital of France is **Paris**. |
| In photosynthesis, plants absorb sunlight to produce ____. | In photosynthesis, plants absorb sunlight to produce **glucose (and oxygen)**. |

---

# Evaluation / Comparison

| Prompt Type | Best For | Strength | Limitation |
|---|---|---|---|
| Straightforward Prompts | Quick facts, definitions, short lists | Fast, unambiguous, easy to write | Limited structure/depth for complex topics |
| Tabular Format Prompting | Comparisons, multi-attribute data | Highly readable, organizes complex data clearly | Not suited for narrative/explanatory answers |
| Preceding Question Prompting | Conceptual understanding, reasoning | Produces richer, context-aware explanations | Slightly longer, less concise responses |
| Missing Word Prompting | Fact recall, fill-in-the-blank testing | Very precise, good for quizzes/assessment | Not suitable for open-ended or complex queries |

---

# Output

### REG NUMBER: 212223030015
### NAME: Janda Hemanth

*Include your Screenshots Here (of prompts executed on the AI tool used):*
- Screenshot 1: Straightforward Prompt outputs
- Screenshot 2: Tabular Format Prompt outputs
- Screenshot 3: Preceding Question Prompt outputs
- Screenshot 4: Missing Word Prompt outputs

---

# Conclusion
The four prompting techniques — Straightforward, Tabular Format, Preceding Question, and Missing Word Prompting — were applied to a common educational use case (renewable energy and environmental science concepts). Each technique demonstrated a distinct strength: straightforward prompts delivered concise facts, tabular prompts organized comparative data clearly, preceding-question prompts elicited deeper conceptual explanations, and missing-word prompts tested precise factual recall. This confirms that selecting the appropriate prompting style based on the nature of the required output significantly improves the quality, clarity, and usefulness of AI-generated responses.

---

# Result
Thus, the prompts for Straightforward, Tabular Format, Preceding Question, and Missing Word Prompting types were written, executed, and evaluated successfully using the chosen use case, and the report was generated accordingly.
