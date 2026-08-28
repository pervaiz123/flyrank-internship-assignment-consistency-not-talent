# Portfolio Impact & Extensibility Plan
**Author:** Pervaiz Ahmed | **Track:** General AI Fluency & Machine Learning

---

## 1. Protocol: "How to Add the Next Case Study" (3-Beat Shape)

To prevent portfolio stagnation and ensure new projects take less than 30 minutes to document and publish, every new case study follows this exact 3-beat structure:

### The 3-Beat Case Template
1. **Beat 1: The Problem (Context & Friction)**
   * What was broken, slow, or unoptimized? 
   * What scale of data or architecture constraints existed?
   * *Example:* "Manual DNS latency diagnostic runs took 4+ hours per domain audit."

2. **Beat 2: What I Did (Technical Execution)**
   * Which tools, libraries, or architectures were deployed?
   * How was target leakage avoided or pipeline efficiency achieved?
   * *Example:* "Engineered asynchronous Python crawlers with LightGBM inference engines across 79M telemetry rows."

3. **Beat 3: What Came of It (Measurable Impact)**
   * What was the final benchmark metric (ROC-AUC, speedup %, accuracy)?
   * Live proof links (deployed paper, demo video, open-source repo).
   * *Example:* "Boosted Page-Rank predictability ROC-AUC from 0.738 to 0.880 (+14.2% lift)."

### Step-by-Step Publishing Workflow
1. Create a new markdown document under `docs/case-studies/` using the 3-beat structure above.
2. Feed raw execution logs and code snippets into the preserved AI Project space to generate clean HTML components matching Netlify site CSS.
3. Add a summary card to `index.html` on [pervaiz-ahmed-ml.netlify.app](https://pervaiz-ahmed-ml.netlify.app/).
4. Run `git commit` and `git push` to trigger automatic continuous deployment via Netlify.

---

## 2. Named Next Real Piece of Work

* **Project Title:** `Real-Time Search Telemetry Streaming & Feature Store (Kafka + LightGBM)`
* **Objective:** Extend the static 79M telemetry capstone into a live streaming inference engine using Apache Kafka, FastAPI, and online feature store validation.
* **Core Stack:** Python, Apache Kafka, FastAPI, LightGBM, Docker.

---

## 3. Evidence of Concrete Reminder Set

To maintain accountability, a recurring calendar notification has been configured:

* **Reminder Title:** `[Portfolio Update] Document & Deploy Kafka Telemetry Case Study`
* **Trigger Date/Time:** September 15, 2026 at 10:00 AM PKT (Recurring every 3 weeks)
* **Platform:** Google Calendar / System Reminders
* **Notification Payload:** *"Check github.com/pervaiz123/ for raw code commits on stream processing; execute 3-beat documentation protocol."*
* **Status:** **Active & Set**

---

## 4. Preserved AI Build Context (Project Environment)

* **Workspace Config:** Claude / Gemini Project Space (`FlyRank-ML-Portfolio-Context`)
* **Retained Voice & Style:** Senior ML/Python Developer tone, zero-fluff, concrete metrics, clear code scaffolding.
* **Identity Kit Preserved:**
  * Resume/Profile link: `https://pervaiz-ahmed-ml.netlify.app/`
  * Target Roles: Junior ML / AI Engineer / Python Developer (International & Remote)
  * Design tokens & CSS formatting used across current Netlify deployment.
* **Maintenance Cost:** **< 15 minutes per case study** (No rebuild required; prompt directly with raw code).
