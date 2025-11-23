ConvNeXT: Robust Brain Tumor Classification on MRI

Overview
This project presents a state-of-the-art deep learning framework that leverages the ConvNeXt Base architecture for highly accurate, efficient, and explainable classification of brain tumors from MRI scans. The model classifies images into four categories: Glioma, Meningioma, Pituitary tumor, and No Tumor, achieving over 99.6% accuracy across diverse datasets. It is designed to balance diagnostic precision, computational efficiency, and interpretability for potential clinical deployment.

Features
Uses modern ConvNeXt Base architecture combining convolutional networks and transformer-inspired design for superior feature extraction.

Cross-dataset validation ensures robust generalization beyond single-domain training.

Extensive benchmarking against ResNet, EfficientNet, VGG, and MobileNet backbones under unified conditions.

Includes post hoc explainability with Grad-CAM and Gradient SHAP visualizations, highlighting clinically relevant tumor regions.

Rigorous statistical tests validate the model’s performance consistency and superiority.

Resource-efficient training with on-the-fly data augmentation and optimized inference speed.

Comprehensive performance metrics reported: accuracy, sensitivity, specificity, precision, recall, F1-score, AUC, and Kappa.

Methodology
ConvNeXt Base architecture customized for brain MRI input, with hierarchical large-kernel depthwise convolutions and Layer Normalization for stable, scalable learning.

Input images preprocessed and resized to 224x224 pixels, then fed through four stages of ConvNeXt blocks with downsampling and feature expansion.

Final classification head with Global Average Pooling and softmax output over four tumor classes.

Trained using Adam optimizer, cross-entropy loss, and regularization strategies such as stochastic depth.

Dataset
Utilizes multiple publicly available MRI brain tumor datasets for training, validation, and external testing.

Classes include Glioma, Meningioma, Pituitary tumors, and No Tumor controls.

Data augmentation applied dynamically to improve model robustness without increasing storage overhead.

Usage
Preprocess MRI images to the required input size and normalization.

Load the trained ConvNeXt model checkpoint.

Run inference to obtain tumor classification probabilities and predicted labels.

Use Grad-CAM or Gradient SHAP tools for explainability visualizations of tumor regions.

Evaluate model using comprehensive metrics provided.

Results and Impact
Consistently outperforms popular CNN backbones with near-perfect accuracy and AUC metrics.

Demonstrated rapid convergence and balanced resource use suitable for clinical or edge deployment.

Explainability maps enhance transparency and trustworthiness for medical professionals.

Validated by multiple statistical significance tests to ensure reliability.

Future Directions
Extend multi-institutional validation and finer tumor subtype classification.

Explore model calibration and fairness evaluation for clinical integration.

Develop deployment pipelines for real-world healthcare applications.

Acknowledgments
Datasets and code repositories are publicly available for reproducibility.

No external funding; authors declare no conflicts of interest.
