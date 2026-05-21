# 🧠 ML-Powered Reminiscence Matching for Dementia Care

> 📄 **Master's Thesis** — Konstantinos Vasilopoulos · Utrecht University · 2024  
> Conducted in collaboration with **[Sports & Memory](https://terugblikken.com)**  
> Full thesis: [`Thesis - Final project.pdf`](Thesis%20-%20Final%20project.pdf)

---

**Business problem:** Matching personal profiles of people living with dementia to relevant sports reminiscence images is done manually by care workers — a slow, inconsistent process that limits the scale of reminiscence therapy.  
**Research question:** Can machine learning automate profile-to-image matching accurately enough to replace manual curation?  
**Finding:** Yes — a lightweight LLM-based text model outperforms both complex fusion approaches and human-intuition baselines, reducing matching from minutes per patient to near-instant.

---

## Why This Matters

Reminiscence therapy — revisiting meaningful memories through images, music, and stories — is one of the most effective non-pharmacological interventions for dementia patients. The bottleneck is **personalisation at scale**: care workers manually match each patient's life history to relevant memory cards, which limits how many patients can benefit.

This project, conducted in partnership with **[Sports & Memory](https://terugblikken.com)**, explores whether ML can close that gap.

---

## Methodology (Plain English)

Three modelling approaches were tested against the same dataset of patient profiles and sports memory cards:

| Approach | What it does |
|---|---|
| **Cosine Similarity Baseline** | Measures text overlap between patient profile and card description using TF-IDF and LLM embeddings |
| **Text-Based ML Models** | Combines text encoders (TF-IDF + 3 LLMs) with regressors (linear, tree-based, distance-based) to predict match quality |
| **Fusion Models** | Adds visual embeddings from pre-trained image encoders to the text models |

4 text encoders were evaluated: TF-IDF, and 3 Large Language Models of varying sizes.

---

## Key Findings

| Finding | Implication |
|---|---|
| Simpler text models outperform complex fusion | Visual features add noise, not signal — the patient's *story* matters more than image content |
| Smaller LLMs beat larger ones | Compact models generalise better on this domain; less overfitting |
| LLMs outperform TF-IDF significantly | Semantic understanding of life events matters — keyword matching misses context |
| Visual fusion did not improve results | Saves infrastructure cost — no image processing pipeline needed in production |

**Recommendation:** Deploy a lightweight LLM-based text encoder paired with a distance-based regressor. This achieves the best accuracy at the lowest computational cost — practical for real-time matching in a care setting.

---

## Dataset

Provided by **Sports & Memory**:
- Personal profiles of dementia patients (demographics, interests, key life events)
- Curated sports memory cards from [terugblikken.com](https://terugblikken.com)
- Match quality scores from human annotators (ground truth)

---

## Repository Contents

| File | Description |
|---|---|
| `Textual_ML_Konstantinos.ipynb.zip` | Full modelling notebook (unzip to run) |
| `Thesis - Final project.pdf` | Complete thesis with methodology and results |
| `README.md` | This file |

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?logo=huggingface&logoColor=black)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikit-learn&logoColor=white)

**Skills demonstrated:** NLP, LLM embeddings, multimodal ML, experimental design, academic research, recommender systems
