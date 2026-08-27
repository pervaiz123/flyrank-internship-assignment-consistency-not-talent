# 5-Minute Showcase Demo Outline & Shareable Cuts

## 5-Minute Showcase Demo Outline

### 1. Question (00:00 - 01:00)
- **Core Challenge:** Can we predict top-decile search visibility using structural domain telemetry without relying on proprietary search query logs?
- **Business Impact:** Solves the FlyRank content discovery problem by identifying technical bottlenecks before content publishing.

### 2. Method (01:00 - 02:15)
- **Dataset:** 79 million rows of public-safe production search metadata.
- **Pipeline:** Engineered domain depth ratios, anchor diversity scores, and DNS response metrics into a LightGBM classification pipeline using an 80/20 leakage-free split.

### 3. One Chart / Key Result (02:15 - 03:30)
- **Model vs. Baseline:** LightGBM achieved **0.880 ROC-AUC** (+14.2% improvement over the 0.738 heuristic baseline) with **0.854 accuracy** and **0.838 precision**.

### 4. One Honest Result & Limitation (03:30 - 04:15)
- **Nuance:** Static crawl snapshots do not account for immediate search engine core updates; high variance remains in non-standard enterprise sites.

### 5. One Recommendation (04:15 - 05:00)
- **Action Playbook (P0):** Sub-200ms DNS first-byte latency is required; response times over 200ms decay crawl indexability by ~18%.

---

## Shareable Cuts

### Cut 1: Social Post (Methodology & Scale Focus)
> How do you predict search visibility across 79 million rows of production search data? 🚀
> 
> During my FlyRank ML Internship, I built a gradient-boosted classification pipeline that predicts top-decile page indexability using structural domain features, crawl dynamics, and DNS telemetry.
> 
> Key highlights:
> 🔹 Engineered 15+ public-safe features (domain depth, anchor metrics, latency thresholds)
> 🔹 Achieved an ROC-AUC of 0.880 (+14.2% lift over traditional heuristic baselines)
> 🔹 Proved that DNS resolution over 200ms drops crawl probability by 18%
> 
> Full research paper & reproducible code live on Netlify & GitHub!
> #MachineLearning #DataScience #Python #LightGBM #SearchIntelligence

### Cut 2: Employer-Facing Summary (3 Sentences)
> Built an end-to-end machine learning pipeline using LightGBM to predict top-decile search visibility across enterprise web pages, evaluated on 79 million rows of production search telemetry. By engineering feature representations for domain authority, URL depth, and DNS crawl latency, the model achieved an ROC-AUC score of 0.880, outperforming heuristic baselines by +14.2%. The research yielded an actionable 3-tier engineering playbook demonstrating that optimizing first-byte latency below 200ms is critical for maximizing search engine crawl rates.
