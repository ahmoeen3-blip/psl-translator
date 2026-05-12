# PSL Translator

> Real-time Pakistan Sign Language to Urdu translator using deep learning.

## 🎯 Project Goal

Deaf Pakistanis ki sign language ko real-time mein Urdu mein translate karna, taa ke woh hospital, bank, schools aur har jagah bina interpreter ke baat kar saken.

## 📊 Current Progress (Day 5/60)

| Experiment | Description | Result |
|------------|-------------|--------|
| **Exp 001** | Zero-shot baseline (VideoMAE-Kinetics) | 85% sign language detection (top-5) |
| **Exp 002** | Fine-tuned classifier (10 classes) | 52.3% validation accuracy (5.2x random) |

## 🛠️ Tech Stack

- **Framework:** PyTorch, HuggingFace Transformers
- **Backbone:** VideoMAE-base (Kinetics-400 pretrained)
- **Dataset:** WLASL-2000 (~21,000 videos)
- **Compute:** Google Colab (T4 GPU)

## 📁 Repository Structure
