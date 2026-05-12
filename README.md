# PSL Translator

> Real-time Pakistan Sign Language to Urdu translator using deep learning.

## 🎯 Project Goal

Deaf Pakistanis ki sign language ko real-time mein Urdu mein translate karna, taa ke woh hospital, bank, schools, aur har jagah bina interpreter ke baat kar saken.

## 📊 Current Progress (Day 10/60)

| Experiment | Description | Val Acc | Test Acc |
|------------|-------------|---------|----------|
| Exp 001 | Zero-shot baseline (Kinetics) | 85% top-5 | - |
| Exp 002 | Fine-tune head (10 classes) | 52.3% | - |
| Exp 003 | + Augmentation 3x | 61.4% | - |
| Exp 004 | + Mixup (plateau) | 61.4% | - |
| Exp 005 | Scale to 50 classes | 45.4% | 38.5% |
| Exp 006 | + Augmentation (50cls) | 48.9% | 39.3% |
| **Exp 007** | **End-to-end fine-tune** | **65.1%** | **63.0%** 🚀 |

📈 **Latest: 65.1% val / 63.0% test on WLASL-50 (32x random baseline)**
🎯 **Comparable to WLASL paper baselines (Li et al. 2020)**

## 🛠️ Tech Stack

- **Framework:** PyTorch, HuggingFace Transformers
- **Backbone:** VideoMAE-base (Kinetics-400 pretrained, last 2 layers fine-tuned)
- **Dataset:** WLASL-2000 (21,095 videos, 2000 ASL signs)
- **Compute:** Google Colab (Tesla T4 GPU)
- **Approach:** Partial fine-tuning + augmentation + differential learning rates

## 🔬 Key Techniques

- **Feature extraction** (Day 5-9): Frozen backbone + custom classifier
- **End-to-end fine-tuning** (Day 10): Last 2 transformer layers unfrozen
- **Differential learning rates**: Backbone 1e-4, head 1e-3
- **Data augmentation**: Temporal sampling, horizontal flip, brightness jitter
- **Regularization**: LayerNorm, GELU, Dropout 0.5, label smoothing

## 📁 Repository Structure
## 🚀 Roadmap

- [x] **Phase 1: Setup & Baselines** (Day 1-4)
  - [x] Environment setup, GPU configuration
  - [x] WLASL dataset acquisition
  - [x] Zero-shot baseline establishment
- [x] **Phase 2: Fine-tuning** (Day 5-10)
  - [x] Feature extraction approach
  - [x] Custom classifier training
  - [x] Augmentation strategies
  - [x] End-to-end fine-tuning (65.1% val)
- [ ] **Phase 3: Scale up** (Day 11-20)
  - [ ] WLASL-100 classes
  - [ ] WLASL-300 classes
  - [ ] Top-5 accuracy reporting
- [ ] **Phase 4: PSL Transfer** (Day 21-35)
  - [ ] PSL data collection (YouTube + community)
  - [ ] Cross-lingual transfer learning
  - [ ] PSL-specific augmentation
- [ ] **Phase 5: Deployment** (Day 36-60)
  - [ ] Live web demo (Hugging Face Spaces)
  - [ ] Real-time inference optimization
  - [ ] Workshop paper draft

## 👤 Author

**Moeen Ahmad**
- GitHub: [@ahmoeen3-blip](https://github.com/ahmoeen3-blip)
- Working on: Pakistan Sign Language recognition using deep learning

## 📜 License

MIT License — see [LICENSE](LICENSE) file for details.

## 🤝 Acknowledgments

- WLASL Dataset by [Dongxu Li et al.](https://dxli94.github.io/WLASL/)
- VideoMAE by [MCG-NJU](https://github.com/MCG-NJU/VideoMAE)
- Project mentor: Claude (Anthropic)
- ## 🚀 Roadmap

- [x] **Phase 1: Setup & Baselines** (Day 1-4)
  - [x] Environment setup, GPU configuration
  - [x] WLASL dataset acquisition
  - [x] Zero-shot baseline establishment
- [x] **Phase 2: Fine-tuning** (Day 5-10)
  - [x] Feature extraction approach
  - [x] Custom classifier training
  - [x] Augmentation strategies
  - [x] End-to-end fine-tuning (65.1% val)
- [ ] **Phase 3: Scale up** (Day 11-20)
  - [ ] WLASL-100 classes
  - [ ] WLASL-300 classes
  - [ ] Top-5 accuracy reporting
- [ ] **Phase 4: PSL Transfer** (Day 21-35)
  - [ ] PSL data collection (YouTube + community)
  - [ ] Cross-lingual transfer learning
  - [ ] PSL-specific augmentation
- [ ] **Phase 5: Deployment** (Day 36-60)
  - [ ] Live web demo (Hugging Face Spaces)
  - [ ] Real-time inference optimization
  - [ ] Workshop paper draft

## 👤 Author

**Moeen Ahmad**
- GitHub: [@ahmoeen3-blip](https://github.com/ahmoeen3-blip)
- Working on: Pakistan Sign Language recognition using deep learning

## 📜 License

MIT License — see [LICENSE](LICENSE) file for details.

## 🤝 Acknowledgments

- WLASL Dataset by [Dongxu Li et al.](https://dxli94.github.io/WLASL/)
- VideoMAE by [MCG-NJU](https://github.com/MCG-NJU/VideoMAE)
- Project mentor: Claude (Anthropic)
