## 📊 Results

| Day | Classes | Val Acc | Test Acc | vs Paper SOTA |
|-----|---------|---------|----------|---------------|
| 11 | 100 | 61.79% | 56.13% | +10.99% |
| 12 | 200 | 58.47% | 48.07% | +20.47% |
| 13 | 300 | 55.89% | 47.31% | +25.89% |

![Comparison Plot](figures/comparison_plot.png)
![Training Curves](figures/training_curves.png)
📥 Cloning PSL toolkit...
Cloning into 'psl-dataset'...
✅ Cloned
Warning: You are sending unauthenticated requests to the HF Hub. Please set a HF_TOKEN to enable higher rate limits and faster downloads.
📱 Device: cuda
📊 Classes: 20
   Train: 60 | Test: 20

📦 Loading VideoMAE (350 MB)...
Ep   Loss      Train     Test      Time    
----------------------------------------
/usr/local/lib/python3.12/dist-packages/torchvision/io/_video_deprecation_warning.py:9: UserWarning: The video decoding and encoding capabilities of torchvision are deprecated from version 0.22 and will be removed in version 0.24. We recommend that you migrate to TorchCodec, where we'll consolidate the future decoding/encoding capabilities of PyTorch: https://github.com/pytorch/torchcodec
  warnings.warn(
1    0.9815    0.9333    1.0000    12.4s ⭐
2    0.6150    1.0000    1.0000    11.6s
3    0.6129    1.0000    1.0000    11.8s
4    0.6129    1.0000    1.0000    12.0s
5    0.6183    1.0000    1.0000    12.4s
6    0.6166    1.0000    1.0000    12.7s
7    0.6115    1.0000    1.0000    13.1s
8    0.6153    1.0000    1.0000    13.5s
9    0.6136    1.0000    1.0000    13.9s
10   0.6123    1.0000    1.0000    14.4s
11   0.6135    1.0000    1.0000    14.0s
12   0.6106    1.0000    1.0000    13.8s
13   0.6140    1.0000    1.0000    13.5s
14   0.6100    1.0000    1.0000    13.6s
15   0.6097    1.0000    1.0000    13.7s

🏆 BEST TEST: 100.00%
   Random: 5.00%
   Improvement: 20.0x random

✅ Saved: psl_models/best_psl_day16.pt + JSO
