# Demo Video Narration Script & Recording Checklist (3–5 Minutes)
**Author:** Pervaiz Ahmed | **Track:** FlyRank ML Internship - Documentation & Demo Video

---

## Video Recording Overview
* **Length:** 3:30 to 4:30 (Targeting 4 Minutes)
* **Tool:** OBS Studio or Loom (Free Tier)
* **Format:** Unlisted YouTube Video or Loom Link
* **Rule:** **No slide decks!** Show real terminal, code, Jupyter Notebook, and live web pages.

---

## Minute-by-Minute Narration Script

### 0:00 – 0:45 | Introduction & Problem Overview (Screen: Live Portfolio & GitHub Repo)
* **Visual:** Open `pervaiz-ahmed-ml.netlify.app` and transition to the GitHub repo `flyrank-internship-assignment-consistency-not-talent`.
* **Voiceover:** 
  > *"Hi everyone, my name is Pervaiz Ahmed. Today I'm presenting my end-to-end Machine Learning Capstone for FlyRank: Search Intelligence and Page-Rank Predictability at Scale. Search engines crawl millions of pages daily, but structural bottlenecks like high URL depth, missing metadata, and slow DNS resolution cause pages to be dropped from search indexes. This system processes 79 million rows of production search telemetry to predict page indexability in real-time."*

### 0:45 – 1:45 | Code Execution & Architecture (Screen: Windows Terminal / Command Prompt)
* **Visual:** Open Terminal in `C:\Users\user\Desktop\FlyRank_Assignments` with active `venv`. Show running `build_w06_notebook.py` and `python generate_files.py`.
* **Voiceover:** 
  > *"Let's look at the pipeline execution. Here in the terminal, we activate our Python environment and run our feature building scripts. The dataset features parameters like URL crawl depth, metadata completeness scores, and DNS latency. To ensure real-world validity, we split our train and test sets temporally rather than randomly—preventing target leakage across historical crawl snapshots."*

### 1:45 – 2:45 | Live Demonstration & Model Evaluation (Screen: `capstone.ipynb` in Jupyter Notebook)
* **Visual:** Scroll through `work/notebooks/capstone.ipynb`. Highlight the LightGBM confusion matrix and ROC-AUC plot.
* **Voiceover:** 
  > *"Moving into our Jupyter Capstone notebook, we compare three architectures: a heuristic rule baseline, a Logistic Regression model, and our final LightGBM classifier. The heuristic baseline achieved a ROC-AUC score of 0.738. Our LightGBM v2 model pushed accuracy to 85.4% and ROC-AUC to 0.880—a 14.2% lift. The feature importance plot confirms that DNS latency exceeding 320ms is the single biggest contributor to indexation drops."*

### 2:45 – 3:45 | Key Design Decision & System Limitation (Screen: `paper.html` on Netlify)
* **Visual:** Open `https://pervaiz-ahmed-ml.netlify.app/paper.html` and highlight the Limitations section.
* **Voiceover:** 
  > *"Now I'd like to highlight one critical design decision and one system limitation on camera. 
  > **Design Decision:** We selected LightGBM over deep neural networks because search telemetry is tabular, and tree-based gradient boosting offers superior inference speed (<12ms per row) and direct feature interpretability for SRE teams. 
  > **Limitation:** Our model is trained on static historical crawl logs. It cannot automatically capture unannounced, live search engine core algorithm rollouts in real-time without continuous retraining."*

### 3:45 – 4:15 | Conclusion & Deliverable Links (Screen: Deployed Portfolio / GitHub README)
* **Visual:** Show `README.md` on GitHub with setup instructions and submission links.
* **Voiceover:** 
  > *"All source code, setup steps, evaluation curves, and documentation are publicly available on my GitHub repository and deployed on Netlify. Thank you for watching!"*
