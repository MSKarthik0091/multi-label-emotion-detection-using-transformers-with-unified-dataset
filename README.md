# Multi-Label Emotion Detection Using Transformers with a Unified Dataset

> Transformer-based multi-label emotion detection using a unified emotion dataset constructed through label harmonization across multiple benchmark datasets.

## 📖 Publication

**Published in the IEEE Xplore Digital Library**

**Conference:** IEEE International Conference on Computer Networks and Inventive Communication Technologies (ICCNCT 2026)

**DOI:** https://doi.org/10.1109/ICCNCT68477.2026.11590520

**IEEE Xplore:** https://ieeexplore.ieee.org/document/11590520

---

# Overview

Understanding human emotions is far more complex than assigning a single emotion to a sentence. A person can simultaneously feel happiness, anxiety, hope, disappointment, or gratitude within the same text. This project formulates emotion detection as a **multi-label classification** problem, allowing multiple emotions to be predicted for a single sentence.

The research investigates how transformer-based language models perform across different emotion datasets and how combining multiple datasets into a unified representation affects generalization, class imbalance, and recognition of nuanced emotions.

Three transformer architectures were evaluated:

- BERT
- RoBERTa
- DistilRoBERTa

The final stage of this work introduces a **Unified Dataset**, created by harmonizing semantically similar emotion labels from multiple datasets into a common label space.

---

# Research Objectives

- Develop a multi-label textual emotion detection system.
- Compare BERT, RoBERTa and DistilRoBERTa under identical experimental settings.
- Study the effect of different datasets on model performance.
- Reduce class imbalance by constructing a unified dataset.
- Improve recognition of rare and fine-grained emotions.
- Evaluate how dataset design influences transformer performance.

---

# Datasets Used

The research utilizes three publicly available datasets.

| Dataset | Emotion Labels |
|---------|---------------:|
| GoEmotions | 28 |
| ISEAR | 7 |
| Emotion Dataset (20 Emotions) | 20 |

Instead of treating these datasets independently, semantically similar labels were harmonized to create a unified dataset containing **30 emotion categories**.

---

# Why are there Four Experimental Sections?

The experiments were intentionally divided into four stages to progressively study how dataset characteristics influence transformer performance.

## Experiment 1 — GoEmotions

The first experiment evaluates BERT, RoBERTa and DistilRoBERTa on the GoEmotions dataset.

Focus:

- Fine-grained emotion recognition
- Neutral class analysis
- Hyperparameter tuning
- Focal Loss for class imbalance

---

## Experiment 2 — ISEAR

The second experiment evaluates RoBERTa and DistilRoBERTa on the ISEAR dataset.

Focus:

- Smaller emotion label space
- Binary Cross Entropy Loss
- Effect of reduced task complexity
- Hyperparameter optimization

---

## Experiment 3 — Combined GoEmotions

The third experiment merges multiple annotation versions of GoEmotions into a richer multi-label representation.

Focus:

- Aggregated annotations
- Increased emotional richness
- Analysis of annotation noise
- Performance comparison against the original GoEmotions dataset

---

## Experiment 4 — Unified Dataset

The final experiment constructs a unified dataset by combining:

- GoEmotions
- ISEAR
- Emotion Dataset (20 Emotions)

using label harmonization.

This stage investigates whether increasing dataset diversity and reducing class fragmentation improves model generalization.

RoBERTa achieved the best overall performance in this experiment.

---

# Experimental Environment

All experiments were conducted using:

- Python
- Google Colab
- NVIDIA GPU acceleration
- Hugging Face Transformers
- PyTorch
- Scikit-learn
- Pandas
- NumPy
- Matplotlib

---

# About the Uploaded Notebooks

The notebooks included in this repository **represent the final and best-performing experimental configurations** used in the research.

During this study, numerous experiments were performed involving different:

- learning rates
- epochs
- token lengths
- dropout values
- weight decay values
- loss functions
- optimizer settings

Only the notebooks corresponding to the **best-performing hyperparameter configurations** have been included in this repository to keep the project concise and reproducible.

---

# Best Results

| Model | Dataset | Micro F1 |
|--------|---------|----------:|
| BERT | GoEmotions | 0.4002 |
| DistilRoBERTa | GoEmotions | 0.4318 |
| RoBERTa | GoEmotions | 0.4342 |
| DistilRoBERTa | ISEAR | 0.6981 |
| RoBERTa | ISEAR | 0.7259 |
| DistilRoBERTa | Combined GoEmotions | 0.5245 |
| RoBERTa | Combined GoEmotions | 0.5273 |
| **RoBERTa** | **Unified Dataset** | **0.6892** |

---

# Future Work

Possible future directions include:

- Sarcasm detection
- Irony detection
- Multimodal emotion recognition
- Ensemble transformer models
- Better handling of minority emotion classes

---

# Author

**Karthikraj M S**

M.Sc. Artificial Intelligence & Data Analytics

Hindustan Institute of Technology and Science

Chennai, India

---
