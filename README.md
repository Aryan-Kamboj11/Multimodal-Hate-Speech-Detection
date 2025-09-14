# Multiclass Multimodal Hate Speech Detection

## Overview
This repository contains the implementation of a deep learning framework for multimodal hate speech identification on social media. The model leverages both textual and visual modalities to improve context understanding and detection accuracy beyond traditional text-only approaches. By utilizing transformer-based architectures and contrastive learning techniques, the framework aims to address the challenges of implicit hate speech conveyed through memes and other multimedia content.

## Key Features
- **Multimodal Architecture**: Combines a transformer-based text encoder (RoBERTa) with a Vision Transformer (ViT) for image feature extraction.
- **Contrastive Learning**: Employs contrastive vision-language pretraining to learn joint representations of text and images.
- **Interpretability**: Designed to provide interpretable results for content moderation.
- **Scalability**: Architecture supports scalability and generalizability across different cultural contexts.
- **Data Augmentation**: Utilizes data augmentation techniques to improve model performance.

## Dataset
The model was trained and evaluated on the **MMHS150K** dataset, a large-scale collection of social media posts annotated for hate speech across multiple categories.

### Performance Metrics
|          | Precision | Recall  | F1 Score | AUC |
|---------------|-----------|---------|----------|---------|
| Proposed without Augmentation     | 0.65    | 0.69  | 0.73   | 0.71     |
| Proposed with Augmentation        | 0.76    | 0.71  | 0.76   | 0.78      |


## Architecture
The proposed framework consists of the following components:
1. **Text Encoder**: A RoBERTa model preprocessed with contrastive loss pretraining.
2. **Image Encoder**: A Vision Transformer (ViT) for extracting image features.
3. **Multimodal Fusion**: Contrastive vision-language pretraining to jointly learn representations from both modalities.

