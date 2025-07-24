# 🧠 Recommender Systems for Dementia-Friendly Sports Reminiscence

This project explores machine learning approaches to support people living with dementia by automatically matching their personal profiles with sports-themed reminiscence images. The goal is to enhance well-being and reduce social isolation through personalized memory-triggering content.

## 📌 Overview

With the ageing population growing worldwide, supporting individuals with dementia is more important than ever. Manual matching of memory cards to personal stories is time-consuming and limits access to reminiscence therapy. This project, in collaboration with **Sports & Memory**, investigates how we can automate this process.

## 🧪 Methods

Three main modeling tracks were compared:

- **Cosine Similarity Baselines**: Using TF-IDF and LLM-based text embeddings to measure profile-card overlap.
- **Text-Based ML Models**: Combining text encoders with regressors (linear, tree-based, and distance-based).
- **Fusion Models**: Incorporating visual embeddings with textual data using pre-trained image encoders.

We tested:
- 4 text encoders (TF-IDF + 3 Large Language Models)
- Memory-based vs. model-based approaches
- Visual + text fusion techniques

## 🔍 Key Findings

- Simpler **text-based models** outperformed more complex fusion approaches.
- **Smaller LLMs** were more effective in model-based learning.
- Visual layers did **not** improve performance.
- **LLMs provided better semantic matching** than TF-IDF and reduced overfitting risk.

## 📂 Dataset

Provided by *Sports & Memory*, the dataset included:
- Rich personal profiles (demographics, interests, life events)
- Curated sports memory cards from [terugblikken.com](https://terugblikken.com)

## 🤝 Acknowledgements

Thanks to **Sports & Memory** for providing data, insight, and collaboration throughout the thesis project.
