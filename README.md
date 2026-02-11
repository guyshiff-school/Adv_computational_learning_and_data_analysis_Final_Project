# Adv_computational_learning_and_data_analysis_Final_Project
Guy Shiff &amp; Muhammad Qais Adv computational learning and data analysis course Final Project

# Attention-Augmented ConvNeXt

Investigating whether adding attention mechanisms to ConvNeXt-Tiny improves image classification.

## Summary

We injected various attention modules (MHSA, SE, ECA, CBAM, Spatial) into pretrained ConvNeXt-Tiny and evaluated on CIFAR-100 and Fashion-MNIST. 

**Key finding:** Attention does NOT help. The baseline without attention consistently outperformed all attention variants.

| Dataset | Baseline | Best Attention | Gap |
|---------|----------|----------------|-----|
| CIFAR-100 | **77.24%** | 75.93% | -1.31% |
| Fashion-MNIST | **94.56%** | 94.43% | -0.13% |

## Conclusions

- Pretrained ConvNeXt features are already strong enough
- ECA achieves same accuracy as MHSA with 6 params vs 592K params
- Convolutional inductive bias dominates over attention for small-image classification
