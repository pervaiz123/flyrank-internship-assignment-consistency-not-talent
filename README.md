# Search Intelligence & Page-Rank Predictability at Scale
> **FlyRank Machine Learning Internship Capstone (FL-01 through FL-10)**  
> **Author:** Pervaiz Ahmed | **Live Paper:** [pervaiz-ahmed-ml.netlify.app/paper.html](https://pervaiz-ahmed-ml.netlify.app/paper.html) | **Portfolio:** [pervaiz-ahmed-ml.netlify.app](https://pervaiz-ahmed-ml.netlify.app/)

---

## Deliverable Index (FL-01 to FL-10)

| Module / Assignment | Deliverable Path / Artifact | Description |
| :--- | :--- | :--- |
| **FL-01: Workflow Audit** | `FL-01_AI_Workflow_Audit/` | Baseline AI development workflow audit and repo setup. |
| **FL-02: Data Pipeline** | `FlyRank_Assignment2_Final_Submission.pdf` | Pipeline architectural design and initial data audit. |
| **FL-03: Proof & Verification** | `FlyRank_Assignment3_What_Are_You_Proving.pdf` | Target definition, baseline selection, and verification suite. |
| **FL-04 - FL-06: Notebooks** | `build_w06_notebook.py`, `build_w07_notebook.py` | Automated feature extraction across 79M telemetry rows. |
| **FL-07: Documentation** | `docs/daily_paper_briefing.md`, `docs/dns-walkthrough.md` | DNS latency analysis and research literature synthesis. |
| **FL-08: Capstone Notebook** | `work/notebooks/capstone.ipynb` | End-to-end model training, validation, and demo cuts. |
| **FL-09: Documentation & Demo** | `README.md`, `submission/demo_link.txt` | Reproducibility guide, v2 eval results, and demo video link. |
| **FL-10: Final Package & Paper** | `paper.html`, `work/retrospective.md`, `submission/paper_url.txt` | Deployed paper, 600-word retrospective, and track sign-off. |

---

## System Overview

This repository implements an end-to-end machine learning system for search engine optimization (SEO) engineering teams. Built on **79 million rows of real production search data** from FlyRank, the model identifies structural bottlenecks (URL depth, metadata completeness, DNS resolution latency) that degrade algorithmic search indexation.

## Reproducible Setup

```bash
git clone [https://github.com/pervaiz123/flyrank-internship-assignment-consistency-not-talent.git](https://github.com/pervaiz123/flyrank-internship-assignment-consistency-not-talent.git)
cd flyrank-internship-assignment-consistency-not-talent
python -m venv venv
venv\\Scripts\\activate
pip install numpy pandas scikit-learn lightgbm matplotlib jupyter
python build_w06_notebook.py
python build_w07_notebook.py
jupyter notebook work/notebooks/capstone.ipynb
```

## v2 Evaluation Results

| Model Architecture | Accuracy | Precision | Recall | ROC-AUC Score | Improvement |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Heuristic Rule Baseline** | 0.724 | 0.681 | 0.650 | 0.738 | Baseline |
| **Logistic Regression (v1)** | 0.789 | 0.752 | 0.731 | 0.812 | +10.0% |
| **LightGBM Classifier (v2)** | **0.854** | **0.838** | **0.812** | **0.880** | **+14.2%** |

## Limitations & Honest Framing

1. **Static Crawl Snapshots:** Historical crawl logs do not dynamically update during live search engine core algorithm rollouts.
2. **Domain Diversity Variance:** Non-standard enterprise architectures exhibit higher residual variance than static sites.
3. **Network Uniformity:** Benchmarking assumes uniform global DNS routing.

## AI Transparency Disclosure

This project was built using **Anthropic Claude and Google Gemini** for code scaffolding and Markdown/HTML structure. All data preprocessing, feature engineering leakage checks, evaluation metrics, and model interpretations were manually verified and executed by **Pervaiz Ahmed**.
