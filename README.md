<h1 align="center"><em>Hyperpigmented Skin Disease Classification Using Deep Learning</em></h1>

### Built with the tools and technologies:

<p align="center">
  <img src="https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/-TensorFlow-FF6F00?logo=tensorflow&logoColor=white" alt="TensorFlow">
  <img src="https://img.shields.io/badge/-Keras-D00000?logo=keras&logoColor=white" alt="Keras">
  <img src="https://img.shields.io/badge/-NumPy-013243?logo=numpy&logoColor=white" alt="NumPy">
  <img src="https://img.shields.io/badge/-Pandas-150458?logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/-Matplotlib-CB3837?logo=matplotlib&logoColor=white" alt="Matplotlib">
  <img src="https://img.shields.io/badge/-Scikit--learn-F7931E?logo=scikit-learn&logoColor=white" alt="Scikit-learn">
</p>

## Introduction

Skin disorders, particularly **skin pigmentation conditions**, are on the rise. **Skin color** is determined by the amount of **melanin** produced in the body, and pigmentation disorders fall into two main categories:

  - **Hyperpigmentation**: Excessive production of melanin, leading to dark spots or patches.
  - **Hypopigmentation**: Reduced melanin, resulting in lighter skin areas.

However, many skin conditions share visual similarities, making it challenging for dermatologists to diagnose them accurately. Early and precise diagnosis can be significantly improved by using **machine learning (ML)** and **deep learning (DL)** techniques, especially when analyzing **dermatoscopy images**.

## Objective

This project investigates the most effective deep learning techniques for identifying and classifying **hyperpigmented skin diseases**. We explore various pre-trained models to determine which method would be most suitable for developing a clinical diagnostic system.

## Models Used

We experimented with five popular **pretrained deep learning models** for classifying four common hyperpigmented skin disorders:

1.  **YOLO**
2.  **DenseNet201**
3.  **GoogLeNet**
4.  **InceptionResNetV2**
5.  **MobileNet**

## Evaluation Metrics

To evaluate the performance of these models, we used the following metrics:

  - **Accuracy**
  - **AUC (Area Under the Curve)**

## Results

After **50 iterations**, the accuracy rates for the models on both the **training set** and **test set** were as follows:

| Model               | Training Set Accuracy | Test Set Accuracy |
|---------------------|-----------------------|-------------------|
| **DenseNet201**      | 100%                  | 87.18%            |
| **GoogLeNet**        | 93.8%                 | 87.18%            |
| **InceptionResNetV2**| 98.77%                | 89.74%            |
| **MobileNet**        | 100%                  | 79.49%            |
| **YOLO**             | 97.43%                | 97.56%            |

## Best Model

Based on our evaluation, **YOLO** was the top-performing model, achieving high accuracy on several skin conditions:

  - **CS** (Condition 1): Excellent performance
  - **MN** (Condition 2): Excellent performance
  - **ML** (Condition 3): Excellent performance
  - **CN** (Condition 4): Excellent performance

Although DenseNet201 demonstrated superior accuracy in the training set, especially with limited datasets, it does not generalize that well in the test set. **YOLO** was selected as the final model for detecting **hyperpigmentation diseases** due to its performance in the **confusion matrix**.

## Conclusion

Our study highlights **DenseNet201** as the best-performing model for accurate classification of hyperpigmented skin conditions, based on both **accuracy** and **AUC**. However, **YOLO** was ultimately chosen due to its effective object detection capability. 

While these models hold great potential as diagnostic tools for dermatologists, further research is needed, including:

  - Expanding the dataset.
  - Exploring hybrid deep learning models to improve clinical accuracy and effectiveness.

## Future Work

  - **Dataset Expansion**: Incorporate a larger variety of skin conditions and images.
  - **Hybrid Model Exploration**: Combine models for more robust detection and classification.
  - **Model Fine-tuning**: Optimize the hyperparameters for real-time clinical applications.

-----

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

Ensure you have Python and pip installed. You will also need the required deep learning libraries (TensorFlow/Keras, NumPy, Pandas, Matplotlib, Scikit-learn).

  * [Python](https://www.python.org/downloads/)
  * [pip](https://pip.pypa.io/en/stable/installation/)

### Installation

1.  Clone the repository:
    ```bash
    git clone [https://github.com/your-username/your-repository.git](https://github.com/your-username/your-repository.git)
    ```
    (Replace with the actual repository URL)
2.  Navigate to the project directory:
    ```bash
    cd Hyperpigmented-Skin-Disease-Classification
    ```
3.  Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```
    (Note: You will need to create a `requirements.txt` file containing all project dependencies like `tensorflow`, `keras`, `numpy`, `pandas`, `matplotlib`, `scikit-learn`, etc.)
4.  Download the dataset (if applicable). Place your dermatoscopy image dataset in the `data/` directory, structured into `train/`, `test/` (and `validation/` if used) subdirectories with class-specific folders.

## Usage

### Training Models

To train the deep learning models:

```bash
python src/train.py
```

(This script should handle data loading, model compilation, and training. You might need to specify model names or hyperparameters as command-line arguments within your script.)

### Evaluating Models

To evaluate the performance of trained models:

```bash
python src/evaluate.py
```

(This script should load trained models and evaluate them on the test set, generating metrics like accuracy and AUC.)

### Making Predictions

To use a trained model for inference on new images:

```bash
python src/predict.py --image_path "path/to/your/image.jpg"
```

(This script should load a trained model and predict the class of a given image.)

-----

## File Structure

The main structure of the project is as follows:

```
.
├── README.md
├── .DS_Store
├── .gitattributes
├── DenseNet201/
├── GoogleNet/
├── InceptionResNetV2/
├── MobileNet/
├── Yolo/
├── RM AUC1.png
└── RM Confussion matrix1.png
```

-----

## License

This project is licensed under the MIT License.
