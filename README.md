# Multi-Class Image Classification Using VGG16

A deep learning project implementing **VGG16 Transfer Learning** with TensorFlow and Keras to classify natural scene images into six categories using the Intel Image Classification dataset.

## Project Overview

This project uses a pre-trained VGG16 convolutional neural network (CNN) as a feature extractor and adds custom classification layers to recognize six types of natural scenes.

**Objective:** Build and evaluate a multi-class image classification model using transfer learning.

## Dataset

The project uses the Intel Image Classification dataset, containing six classes:

- Buildings
- Forest
- Glacier
- Mountain
- Sea
- Street

| Dataset | Number of Images |
|---|---:|
| Training | 14,034 |
| Testing | 3,000 |
| Total labeled images | 17,034 |

The unlabeled prediction dataset is not used for model training or evaluation.

## Model Architecture

The model is based on VGG16 pretrained on ImageNet.

Architecture:

1. Pre-trained VGG16 convolutional base
2. Global Average Pooling
3. Dense layer (256 neurons, ReLU)
4. Dropout (0.5)
5. Output layer (6 neurons, Softmax)

The VGG16 base is frozen during the baseline training stage.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

## Baseline Hyperparameters

| Parameter | Value |
|---|---|
| Model | VGG16 |
| Input size | 224 × 224 × 3 |
| Batch size | 32 |
| Learning rate | 0.0001 |
| Optimizer | Adam |
| Loss function | Categorical Crossentropy |
| Epochs | 10 |
| Dropout | 0.5 |

## Baseline Results

| Metric | Result |
|---|---:|
| Training Accuracy | 91.87% |
| Validation Accuracy | 92.84% |
| Test Accuracy | **91.27%** |
| Test Loss | 0.2480 |

## Results and Visualizations

The following evaluation outputs are available in the `results/` directory:

- Training and validation accuracy/loss curves
- Confusion matrix
- Classification report

## Repository Structure

```text
vgg16-image-classification/
│
├── notebooks/
│   └── VGG16_Image_Classification.ipynb
│
├── results/
│   ├── accuracy_loss_curves.png
│   ├── confusion_matrix.png
│   └── classification_report.txt
│
├── README.md
└── ...
```

## Future Improvements

- Conduct hyperparameter ablation experiments.
- Compare different dropout rates and learning rates.
- Experiment with fine-tuning selected VGG16 layers.
- Analyze the impact of model configurations on classification performance.

## Author

**Muhammad Attiq**

Computer Engineering Student | AI & Machine Learning Enthusiast

[GitHub](https://github.com/Muhammad-Attiq)

---

*This project was developed as part of a deep learning academic assignment and is intended to demonstrate practical experience with CNNs, transfer learning, and model evaluation.*
