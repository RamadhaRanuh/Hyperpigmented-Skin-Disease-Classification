# Hyperpigmented Skin Disease Classification Using Deep Learning

## Introduction

Skin disorders, particularly **skin pigmentation conditions**, are on the rise. **Skin color** is determined by the amount of **melanin** produced in the body, and pigmentation disorders fall into two main categories:

- **Hyperpigmentation**: Excessive production of melanin, leading to dark spots or patches.
- **Hypopigmentation**: Reduced melanin, resulting in lighter skin areas.

However, many skin conditions share visual similarities, making it challenging for dermatologists to accurately diagnose them. Early and precise diagnosis can be significantly improved by using **machine learning (ML)** and **deep learning (DL)** techniques, especially when analyzing **dermatoscopy images**.

## Objective

This project investigates the most effective deep learning techniques for the identification and classification of **hyperpigmented skin diseases**. We explore various pre-trained models to determine which method would be most suitable for developing a clinical diagnostic system.

## Models Used

We experimented with five popular **pretrained deep learning models** for classifying four common hyperpigmented skin disorders:

1. **YOLO**
2. **DenseNet201**
3. **GoogLeNet**
4. **InceptionResNetV2**
5. **MobileNet**

## Evaluation Metrics

To evaluate the performance of these models, we used the following metrics:

- **Accuracy**
- **AUC (Area Under the Curve)**

## Results

After **50 iterations**, the accuracy rates for the models on both the **training set** and **test set** were as follows:

| Model               | Training Set Accuracy | Test Set Accuracy |
|---------------------|-----------------------|-------------------|
| **DenseNet201**      | 100%                  | 87.18%            |
| **GoogLeNet**        | 93.8%                 | 87.18%            |
| **InceptionResNetV2**| 98.77%                | 89.74%            |
| **MobileNet**        | 100%                  | 79.49%            |
| **YOLO**             | 97.43%                | 97.56%            |

## Best Model

Based on our evaluation, **DenseNet201** was the top-performing model, achieving high accuracy on several skin conditions:

- **CS** (Condition 1): Excellent performance
- **MN** (Condition 2): Excellent performance
- **ML** (Condition 3): Excellent performance
- **CN** (Condition 4): Moderate performance

Although DenseNet201 demonstrated superior generalization, especially with limited datasets, **YOLO** was selected as the final model for detecting **hyperpigmentation diseases** due to its performance in the **confusion matrix**.

## Conclusion

Our study highlights **DenseNet201** as the best performing model for accurate classification of hyperpigmented skin conditions, based on both **accuracy** and **AUC**. However, **YOLO** was ultimately chosen due to its effective object detection capability. 

While these models hold great potential as diagnostic tools for dermatologists, further research is needed, including:

- Expanding the dataset.
- Exploring hybrid deep learning models to improve clinical accuracy and effectiveness.

## Future Work

- **Dataset Expansion**: Incorporate a larger variety of skin conditions and images.
- **Hybrid Model Exploration**: Combine models for more robust detection and classification.
- **Model Fine-tuning**: Optimize the hyperparameters for real-time clinical applications.

---

