# Multi-Class Defect Detection in Civil Infrastructure Using Deep Learning

## Overview
This project presents a deep learning–based framework for **multi-class
defect detection and semantic segmentation** in civil infrastructure.
The work is based on my MSc dissertation at Ulster University and builds
directly on established academic research in large-scale infrastructure
defect segmentation.

Unlike single-defect approaches, this project addresses the realistic
scenario where **multiple types of deterioration coexist** within the
same structure, enabling more comprehensive and objective condition
assessment.

## Research Background
This work is inspired by and builds upon the **DACL10k dataset and
benchmark study**, which provides one of the largest annotated datasets
for defect segmentation in concrete infrastructure.

The research demonstrates the feasibility of **multi-class semantic
segmentation** for infrastructure inspection and highlights challenges
such as extreme class imbalance, thin-object segmentation, and noisy
annotations.

## Civil Engineering Problem
Traditional infrastructure inspections rely heavily on manual visual
assessment. In practice, inspectors must identify and classify several
defect types simultaneously, including cracks, corrosion, spalling, and
surface degradation.

This process is:
- Time-consuming
- Subjective
- Difficult to standardise across inspectors and assets

Automated multi-class defect detection provides a scalable and objective
solution for structural health monitoring and asset management.

## Objectives
- Detect and segment multiple concrete defect types from inspection images
- Replicate and evaluate academic benchmark performance in practice
- Investigate model robustness under real-world inspection conditions
- Support future integration with BIM and digital twin systems

## Defect Classes
The model targets multiple defect and contextual classes, including:
- Cracks
- Spalling
- Corrosion
- Efflorescence
- Wet spots
- Surface weathering
- Structural and contextual elements (e.g. drainage, equipment, joints)

## Methodology
The proposed pipeline follows a semantic segmentation approach:
- Image preprocessing and data augmentation
- Feature extraction using an EfficientNet-B4 backbone
- Multi-scale feature fusion using a Feature Pyramid Network (FPN)
- Multi-class training using combined Cross-Entropy and Dice loss
- Performance evaluation using mIoU, Precision, Recall, and F1-score

This methodology closely follows the reference academic work while being
adapted for practical engineering inspection scenarios.

## Models and Tools
- Python 3.11
- PyTorch
- segmentation-models-pytorch
- EfficientNet-B4
- Feature Pyramid Network (FPN)
- Albumentations
- OpenCV

## Dataset
- DACL10k multi-class defect dataset (18 classes)
- Real-world inspection images from operational infrastructure projects

Due to dataset size, licensing, and ownership restrictions, **only sample
images are included** in this repository.

## Results
The trained model demonstrates:
- Strong performance on object-like defect classes
- Reasonable generalisation to real inspection images
- Reduced performance for thin and minority classes such as cracks,
  consistent with findings reported in the reference paper

Qualitative segmentation outputs and representative predictions are
available in the `results/` directory.

## Engineering Impact
- Enables automated, multi-defect infrastructure inspection
- Reduces subjectivity in defect classification
- Supports large-scale asset condition assessment
- Contributes to digital inspection and maintenance workflows

## Limitations and Future Work
- Performance is constrained by severe class imbalance in the dataset
- Crack segmentation accuracy remains lower than single-defect models
- Future work will explore transformer-based architectures, class-aware
  loss functions, and higher-resolution training strategies

## References
- DACL10k: Benchmark Dataset and Baseline for Multi-Class Defect Detection
  in Concrete Infrastructure
- Related work on semantic segmentation for structural health monitoring

## Author
Mohamed Ragab 
MSc Research – Ulster University  
Multi-Class Defect Detection for Structural Health Monitoring
