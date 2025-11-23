# ConVNest: Brain Tumor Classification on MRI Scans

<img width="329" height="359" alt="m" src="https://github.com/user-attachments/assets/d50b5282-c151-4266-9451-f19d7aa0fd54" />

## Project Summary
This project develops a robust and efficient deep learning framework for multi-class brain tumor classification using MRI images. Leveraging a modernized ConvNeXt Base architecture inspired by transformer designs, the model classifies brain tumors into four categories: Glioma, Meningioma, Pituitary tumor, and No Tumor. It achieves exceptional accuracy (>99.6%) and reliable generalization across multiple independent datasets while providing explainable predictions through visualization techniques like Grad-CAM and Gradient SHAP.

## Key Achievements

- Adapted and optimized the ConvNeXt Base model for medical imaging focused on brain MRI.
- Comprehensive cross-dataset validation demonstrating strong generalization beyond single-domain data.
- Benchmarking against leading CNN architectures (ResNet152, EfficientNetV2-B0, VGG19, MobileNetV3 Large) under uniform conditions.
- Applied rigorous statistical tests (Friedman, Holm, Wilcoxon, Kendall's W) to validate model performance.
- Integrated efficient on-the-fly data augmentation to improve robustness without storage overhead.
- Delivered computational efficiency profiling suitable for clinical and edge deployment considerations.
- Provided multi-perspective interpretability validating model focus on clinically relevant tumor regions using explainability methods.

## Methodology
- Employed ConvNeXt Base convolutional architecture with large kernel depthwise convolutions and layer normalization.
- Input MRI slices resized to 224x224 resolution and passed through hierarchical ConvNeXt blocks across four stages.
- Final classification head utilizes Global Average Pooling and softmax layers for four-class prediction.
- Trained using Adam optimizer with categorical cross-entropy loss, over 20 epochs with batch size 32.
- Implemented stochastic depth regularization and transfer learning from pretrained weights.

## Dataset and Preprocessing
- Utilized publicly available heterogeneous MRI brain tumor datasets spanning multiple institutions.
- Classes include Glioma, Meningioma, Pituitary, and No Tumor cases.
- Performed dynamic resizing, normalization, and data augmentation (rotations, flips, crops) on-the-fly during training.

## Usage Instructions
- Preprocess MRI scans to normalized 224x224 size.
- Load the pretrained ConvNeXt Base model checkpoint.
- Perform inference to obtain tumor class probabilities and predicted labels.
- Visualize decision regions using Grad-CAM or Gradient SHAP for explainability.
- Evaluate performance using metrics like accuracy, precision, recall, F1-score, AUC, and kappa statistics.

## References and Resources
- Dataset and code repositories are publicly available for reproducibility.
- Detailed architecture design, training scripts, and evaluation notebooks included.

---

This README reflects the comprehensive work on the ConvNeXt-based brain tumor classification framework with a focus on accuracy, efficiency, explainability, and clinical relevance.


