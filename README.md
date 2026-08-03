## Name: Janda Hemanth
## Reg No: 212223030015

---

# Ex. No: 4
# Date:

# Advanced Prompt Engineering Techniques

---

# Aim
To implement and evaluate advanced prompt engineering techniques — Zero-Shot Prompting, Few-Shot Prompting, Chain of Thought, Persona Pattern, Reverse Prompting, Graph Prompting, and Active Prompting — using engineering case studies (Smart Irrigation, Drone Navigation, Robot Path Planning), and to evaluate the outputs based on Reasoning, Correctness, and Token Usage.

---

# Problem Statement
Advanced engineering problems often require an AI system to reason through multi-step logic, weigh trade-offs, and produce technically accurate outputs — not just retrieve simple facts. Different prompting techniques influence how well an AI model handles this complexity: some techniques improve reasoning depth, others improve output structure, and others reduce ambiguity by having the model ask clarifying questions itself. This experiment applies seven advanced prompting techniques to three real-world engineering case studies — Smart Irrigation Systems, Drone Navigation, and Robot Path Planning — to compare their effectiveness in terms of reasoning quality, correctness of the technical solution, and token (computational) efficiency.

---

# Algorithm / Procedure

### Step 1: Select Engineering Case Studies
- **Case Study 1:** Smart Irrigation System (sensor-based water management)
- **Case Study 2:** Drone Navigation (autonomous flight path and obstacle avoidance)
- **Case Study 3:** Robot Path Planning (shortest/safest path in a grid or dynamic environment)

### Step 2: Define and Apply Each Prompting Technique
Apply each of the seven techniques to the most suitable case study (as detailed below), recording the exact prompt and the generated response.

### Step 3: Record Token Usage
- Count/estimate the number of input and output tokens for each prompt-response pair using the platform's usage metadata or a tokenizer tool.

### Step 4: Evaluate Each Output
- Rate each response on a 1–5 scale for **Reasoning** (depth/logical soundness), **Correctness** (technical accuracy), and note **Token Usage** (efficiency).

### Step 5: Compare and Conclude
- Tabulate results across all seven techniques and identify which technique(s) are best suited for which type of engineering problem.

---

# Implementation

### 1. Zero-Shot Prompting
**Case Study:** Smart Irrigation
**Prompt:** "Design a basic smart irrigation system using soil moisture sensors. List the main components and how they interact."

**Response (Summary):** A smart irrigation system typically includes a soil moisture sensor, a microcontroller (e.g., Arduino/ESP32), a water pump with relay control, and optionally a cloud dashboard. The sensor continuously monitors soil moisture; when it drops below a threshold, the microcontroller activates the relay to turn on the pump until moisture returns to the desired level.

**Observation:** Correct at a general level but lacks depth on edge cases (e.g., sensor calibration, weather integration).

---

### 2. Few-Shot Prompting
**Case Study:** Drone Navigation
**Prompt:** "Example: For obstacle avoidance in a warehouse robot, we use LIDAR + a potential field algorithm to steer away from obstacles in real time. Now, using a similar style, explain how a drone can navigate and avoid obstacles indoors."

**Response (Summary):** Following the same reasoning pattern, an indoor drone can use a combination of ultrasonic/LIDAR sensors and a potential field algorithm, where obstacles generate repulsive forces and the goal generates an attractive force, guiding the drone along a collision-free path while adjusting altitude for 3D obstacles like shelves or beams.

**Observation:** The example primed the model to produce a more analogous, technically consistent answer than zero-shot alone.

---

### 3. Chain of Thought (CoT)
**Case Study:** Robot Path Planning
**Prompt:** "A robot needs to move from point A to point B in a grid with obstacles. Think step-by-step: first identify possible pathfinding algorithms, then explain why one is best suited, then describe how it would be implemented."

**Response (Summary):**
*Step 1:* Candidate algorithms — BFS, Dijkstra's, A* Search.
*Step 2:* A* is best suited because it uses a heuristic (e.g., Manhattan distance) to prioritize promising paths, making it faster than BFS/Dijkstra's for grid-based navigation with known goal coordinates.
*Step 3:* Implementation — represent the grid as nodes, assign cost `g(n)` from start and heuristic `h(n)` to goal, expand nodes in order of `f(n) = g(n) + h(n)`, and backtrack from the goal once reached to reconstruct the path.

**Observation:** Strongest reasoning depth; clearly justified the algorithm choice before implementation.

---

### 4. Persona Pattern
**Case Study:** Smart Irrigation
**Prompt:** "You are a senior agricultural IoT engineer. Explain to a farmer with no technical background how a smart irrigation system saves water, in simple, non-technical language."

**Response (Summary):** "Think of it like a system that constantly checks how thirsty your soil is. Instead of watering on a fixed schedule, it only turns on the water when the soil actually needs it — so you're not wasting water on rainy days or over-watering when it's not needed. Over time, this can cut water usage significantly while keeping your crops healthy."

**Observation:** Highest simplicity/user-experience score; ideal for non-technical stakeholders, though technical depth was intentionally reduced.

---

### 5. Reverse Prompting
**Case Study:** Drone Navigation
**Prompt:** "I want to design an autonomous drone navigation system, but before answering, ask me any clarifying questions you need about the environment, payload, and constraints."

**Response (Summary):** The model responded with clarifying questions such as: "Will the drone operate indoors or outdoors? What sensors are available (GPS, LIDAR, camera)? What is the maximum flight time/battery capacity? Are there dynamic (moving) obstacles to avoid?" — before proceeding to a tailored design once these were answered.

**Observation:** Reduced ambiguity significantly; particularly useful for underspecified engineering requirements, though it added an extra interaction round (higher token usage overall).

---

### 6. Graph Prompting
**Case Study:** Robot Path Planning
**Prompt:** "Represent the robot's environment as a graph: nodes are grid cells, edges connect walkable neighboring cells with a cost of 1, and obstacles have no edges. Using this graph representation, explain how Dijkstra's algorithm finds the shortest path from node A to node B."

**Response (Summary):** The model described the grid as a weighted graph `G = (V, E)`, where each node's shortest distance from the start is initialized to infinity except the start node (0). It then explained the iterative relaxation process: repeatedly selecting the unvisited node with the smallest tentative distance, updating its neighbors' distances, and marking it visited, until the goal node is reached — producing the shortest path via backtracking through recorded predecessors.

**Observation:** Explicit graph framing improved structural precision and made the algorithmic explanation more rigorous and implementation-ready.

---

### 7. Active Prompting
**Case Study:** Smart Irrigation
**Prompt:** "Here are three possible irrigation control strategies: (1) fixed schedule, (2) threshold-based sensor control, (3) predictive ML-based control using weather forecasts. Rank these by water efficiency, explain your uncertainty for each ranking, and ask me if you need real deployment data to refine the ranking."

**Response (Summary):** The model ranked: (1) Predictive ML-based control — highest efficiency but highest uncertainty without real data; (2) Threshold-based sensor control — moderately efficient, low uncertainty; (3) Fixed schedule — least efficient, well understood. It then asked whether local rainfall data or crop-specific water requirements were available to refine the ranking further.

**Observation:** Actively flagged uncertainty and requested the most informative missing data — well suited for decision-support scenarios with incomplete information.

---

# Evaluation Table

| Technique | Case Study | Reasoning (1–5) | Correctness (1–5) | Token Usage (Approx.) | Notes |
|---|---|---|---|---|---|
| Zero-Shot | Smart Irrigation | 3 | 4 | Low (~120 tokens) | Fast but shallow |
| Few-Shot | Drone Navigation | 4 | 4 | Medium (~200 tokens) | Better stylistic/technical consistency |
| Chain of Thought | Robot Path Planning | 5 | 5 | High (~320 tokens) | Best reasoning depth, justified choices |
| Persona Pattern | Smart Irrigation | 3 | 4 | Low (~140 tokens) | Best for non-technical communication |
| Reverse Prompting | Drone Navigation | 4 | 5 | High (~350 tokens, multi-turn) | Reduces ambiguity, costs extra turns |
| Graph Prompting | Robot Path Planning | 5 | 5 | Medium-High (~280 tokens) | Most structurally rigorous |
| Active Prompting | Smart Irrigation | 4 | 4 | Medium (~230 tokens) | Good uncertainty handling |

*(Token counts are illustrative approximations for demonstration; actual values should be measured using the target platform's tokenizer/usage metadata.)*

---

# Comparison of Techniques

| Technique | Best Suited For | Trade-off |
|---|---|---|
| Zero-Shot | Quick, well-known technical queries | Limited depth for complex/multi-step problems |
| Few-Shot | Maintaining consistent style/format | Requires good example curation |
| Chain of Thought | Multi-step algorithmic/engineering reasoning | Higher token usage, longer responses |
| Persona Pattern | Communicating technical content to non-experts | May sacrifice technical precision |
| Reverse Prompting | Underspecified or ambiguous requirements | Extra interaction rounds increase cost |
| Graph Prompting | Structured/relational problems (pathfinding, networks) | Requires the problem to be graph-representable |
| Active Prompting | Decision-making under uncertainty | Needs follow-up data to fully resolve rankings |

---

# Output

### REG NUMBER: 212223030015
### NAME: Janda Hemanth

*Include your Screenshots Here:*
- Screenshot 1: Zero-Shot & Few-Shot prompt outputs
- Screenshot 2: Chain of Thought reasoning trace
- Screenshot 3: Persona Pattern response
- Screenshot 4: Reverse Prompting clarifying-question exchange
- Screenshot 5: Graph Prompting structured explanation
- Screenshot 6: Active Prompting ranking with uncertainty
- Screenshot 7: Token usage panel/metadata from the AI platform

---

# Conclusion
Seven advanced prompting techniques were implemented across three engineering case studies — Smart Irrigation, Drone Navigation, and Robot Path Planning. **Chain of Thought** and **Graph Prompting** produced the strongest reasoning and correctness for algorithmically structured problems like path planning, at the cost of higher token usage. **Reverse Prompting** proved most effective at resolving ambiguous requirements before generating a solution, while **Active Prompting** was most useful for ranking options under uncertainty. **Persona Pattern** excelled at simplifying technical content for non-expert audiences, and **Zero-Shot**/**Few-Shot** remained the most token-efficient choices for straightforward technical queries. This confirms that technique selection should be guided by the nature of the engineering problem — favoring reasoning-heavy techniques for complex algorithmic tasks and lighter techniques for simple, well-defined queries.

---

# Result
Thus, the advanced prompt engineering techniques — Zero-Shot, Few-Shot, Chain of Thought, Persona Pattern, Reverse Prompting, Graph Prompting, and Active Prompting — were successfully implemented on engineering case studies and evaluated in terms of Reasoning, Correctness, and Token Usage.
