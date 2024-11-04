# TIGER: Time-frequency Interleaved Gain Extraction and Reconstruction for Efficient Speech Separation
### Abstract

In recent years, much speech separation research has focused primarily on improving model performance. However, for low-latency speech processing systems, computational efficiency is equally critical. In this paper, we propose a speech separation model with significantly reduced parameter size and computational cost: *Time-Frequency Interleaved Gain Extraction and Reconstruction Network (TIGER)*. TIGER leverages prior knowledge to divide frequency bands and applies compression on frequency information. We employ a multi-scale selective attention (MSA) module to extract contextual features, while introducing a full-frequency-frame attention (F^3A) module to capture both temporal and frequency contextual information. Additionally, to more realistically evaluate the performance of speech separation models in complex acoustic environments, we introduce a novel dataset called *EchoSet*. This dataset includes noise and more realistic reverberation (e.g., considering object occlusions and material properties), with speech from two speakers overlapping at random proportions. Experimental results demonstrated that TIGER significantly outperformed state-of-the-art (SOTA) model TF-GridNet on the EchoSet dataset in both inference speed and separation quality, while reducing the number of parameters by **94.3%** and the MACs by **95.3%**. These results indicate that by utilizing frequency band-split and interleaved modeling structures, TIGER achieves a substantial reduction in parameters and computational costs while maintaining high performance. Notably, TIGER is the first speech separation model with fewer than **1 million parameters** that achieves performance close to the SOTA model.

### Usage

Training:

`python audio_train.py --conf_dir configs/tiger.yml`

Inference:

`python audio_test.py --conf_dir configs/tiger.yml`
