
---

# Project: AI-Home Care Orchestrator
**Objective:** A Fullstack AI application that acts as an intelligent bridge between elderly care and home automation, utilizing Agentic AI to manage IoT devices via natural language.

---

## 🏗️ Phase 1: Architecture & Data Modeling
*Focus: System Design and logic over aesthetics.*

* **Core Tech Stack:**
    * **Frontend:** Next.js (App Router), Tailwind CSS.
    * **Backend:** Node.js (Express) or Next.js API Routes.
    * **AI:** OpenAI SDK or LangChain (for Agentic workflows).
    * **Connectivity:** Cloudflare Tunnels (to expose local IoT endpoints).
* **Data Structure:** Define a `Device` object.
    ```json
    {
      "id": "lg-tv-001",
      "name": "Living Room TV",
      "type": "Entertainment",
      "status": "online",
      "power": "off"
    }
    ```

---

## 🧠 Phase 2: The "Brain" (Backend & AI Agent)
*Focus: Asynchronous JavaScript and API Design.*

* **Task 1: Mock IoT API:** Build REST endpoints (`GET /api/devices`, `POST /api/device/control`) to simulate hardware interaction.
* **Task 2: AI Tool Definition:** Implement **Function Calling**. 
    * Define a tool called `updateDeviceState(id, action)`.
    * Configure the LLM to recognize when a user says "Turn off the TV" and return the specific function arguments instead of just text.
* **Task 3: Logic Flow:**
    * User Input → LLM Analysis → Function Trigger → Backend State Change → Success Response.

---

## 💻 Phase 3: The "Face" (Frontend Development)
*Focus: React State Management and UX.*

* **Task 1: Device Dashboard:** Use `.map()` to render device cards. Practice clean destructuring of props.
* **Task 2: State Synchronization:** Implement React `useState` and `useEffect` to ensure the UI updates immediately when the AI agent toggles a device.
* **Task 3: The "Command Center":** Build a chat interface.
    * Include "Loading" states for AI thinking time.
    * Handle errors gracefully (e.g., "I couldn't reach the TV right now").

---

## 🛠️ Phase 4: Senior-Level Optimization
*Focus: Professional standards and "Interview-Ready" features.*

* **Validation:** Use TypeScript (optional but recommended) to define interfaces for your API responses.
* **Security:** Implement environment variables (`.env`) for API keys—never hardcode them.
* **Performance:** Optimize Next.js components (Server vs. Client components).
* **Edge Case Handling:** What happens if the AI receives an ambiguous command like "Make it comfy"? (Hint: Program the Agent to ask clarifying questions).

---

## 📈 Daily Integration (The "Rust-Remover" Routine)
*To be done alongside the project to stay sharp for interviews.*

1.  **Morning (30m):** 1 DSA problem in JavaScript (Arrays/Strings) to maintain "Syntax Memory."
2.  **Evening (1h):** Execute one "Task" from the phases above. 
3.  **Weekly:** Document one "Challenge" you faced and how you solved it. (This becomes your talking point in interviews).

---

### ✅ Success Criteria
* [ ] I can explain the data flow from the UI to the LLM.
* [ ] The application handles "Async" operations without crashing.
* [ ] The code is clean, modular, and free of unnecessary jargon.
* [ ] The AI Agent can successfully control at least two mock devices.

---