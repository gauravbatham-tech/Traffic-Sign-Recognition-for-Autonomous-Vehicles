**Traffic Sign Recognition for Autonomous Vehicles**

This project focuses on building an industry-grade traffic sign recognition system using deep learning. It was developed as part of an AI/ML internship to understand image preprocessing, class imbalance handling, transfer learning, model evaluation, and real-time deployment.

**📂 Project Overview****

Traffic sign recognition is a core component of autonomous driving systems. The objective of this project is to train a robust model capable of classifying traffic signs from image data (GTSRB dataset). The pipeline includes preprocessing, augmentation, transfer learning, fine-tuning, explainability, and real-time inference.

**This notebook includes:**

Dataset loading from Google Drive

Image preprocessing and realistic augmentation

Balanced sampling for imbalanced classes

Training a deep CNN using EfficientNetV2

Fine-tuning for improved accuracy

Evaluation using classification report, macro-F1, and confusion matrix

Grad-CAM++ visualization for explainability

ONNX model export for deployment

Real-time inference using webcam

**⚙️ Tech Stack**

Language: Python
Libraries: TensorFlow, Keras, OpenCV, NumPy, Matplotlib, Seaborn, Scikit-learn, tf2onnx
Tools: Google Colab
Dataset: German Traffic Sign Recognition Benchmark (GTSRB)

**DATASET:** https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign

**🚀 Implementation Steps**
1. Data Loading & Verification

Mounted Google Drive and loaded the dataset folders (Train, Test, Meta)

Verified class folders and checked dataset integrity

2. Preprocessing & Augmentation

Resized images to 128×128

Normalized pixel values

Applied strong augmentations for real-world robustness (rotation, zoom, brightness, translation)

3. Handling Class Imbalance

Computed sample counts per class

Applied class weights during training to prevent bias

4. Model Development

Used EfficientNetV2B0 as the feature extractor

Added global pooling, dropout, and classification head

Trained in two stages: frozen-base training → full fine-tuning

5. Model Evaluation

Tested on the separate test set using:

Classification report

Macro-F1 score

Confusion matrix heatmap

6. Explainability (Grad-CAM++)

Implemented Grad-CAM++ to visualize model focus regions

Helps interpret predictions and increases trust

7. Model Export

Exported the trained model to ONNX format for deployment

Ensures compatibility with edge devices and optimized runtimes

8. Real-Time Inference

Implemented webcam-based live traffic sign prediction

Added FPS-friendly inference loop using OpenCV

**📊 Results**

Stable training with balanced sampling

Improved accuracy after fine-tuning

Clear confusion matrix visualization

Grad-CAM++ shows strong focus on the correct traffic sign region

ONNX export enables lightweight deployment

**🏁 Conclusion**

This project demonstrates a complete, industry-ready pipeline for traffic sign recognition—from data preprocessing to real-time deployment. It highlights the importance of augmentation, balanced learning, explainability, and exportability for real-world autonomous driving applications.
