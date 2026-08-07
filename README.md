# 🧠 Brain Tumor MRI Classification using a Custom CNN

A deep learning project that implements a **Custom Convolutional Neural Network (CNN)** with **Residual Skip Connections** for multiclass **Brain Tumor MRI Classification**.

The model was developed using **TensorFlow/Keras** and trained on the **Brain Tumor MRI Dataset** to classify MRI scans into four categories:

- Glioma
- Meningioma
- No Tumor
- Pituitary Tumor

Unlike transfer learning approaches, this project demonstrates the design of a CNN built entirely from scratch, incorporating **Residual Connections**, **Swish Activation**, **Batch Normalization**, and **L2 Regularization** to improve feature learning and optimization.

---

# 🎯 Model Performance

| Metric | Score |
|--------|-------:|
| **Training Accuracy** | **99.97%** |
| **Validation Accuracy** | **94.11%** |
| **Test Accuracy** | **89.13%** |

The model achieves strong feature learning while demonstrating the challenges of generalization on unseen MRI images.

---

# 📂 Project Structure

```text
Brain-Tumor-Classification-Custom-CNN/
│
├── Brain_Tumor_Custom_CNN.ipynb
├── README.md
│
├── images/
│   ├── accuracy_curve.png
│   ├── loss_curve.png

```

---

# ⚙️ Requirements

Install the required libraries:

```bash
pip install tensorflow numpy pandas matplotlib seaborn scikit-learn
```

### Dependencies

- Python 3.x
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

# 📥 Dataset

The project uses the **Brain Tumor MRI Dataset** available on Kaggle.

**Dataset Link**

https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

### Dataset Classes

| Class |
|--------|
| Glioma |
| Meningioma |
| No Tumor |
| Pituitary |

**Total Classes:** 4

---

# 🏗️ Model Architecture

The proposed CNN architecture consists of:

- Input Layer
- Image Rescaling
- Residual Skip Connection
- Three Convolutional Feature Extraction Blocks
- Batch Normalization
- Swish Activation
- Max Pooling
- Dropout Regularization
- Flatten Layer
- Fully Connected Layer (128 neurons)
- Softmax Output Layer (4 Classes)

---

# 🧠 Network Architecture

### Residual Block

- Input
- 1×1 Convolution (Shortcut)
- Batch Normalization
- 3×3 Convolution
- Batch Normalization
- Residual Addition
- Swish Activation
- MaxPooling2D

### Feature Extraction Block

- Conv2D (64 Filters)
- Conv2D (64 Filters)
- Batch Normalization
- Swish Activation
- MaxPooling2D
- Dropout (0.20)

### Deep Feature Block

- Conv2D (128 Filters)
- Conv2D (128 Filters)
- Batch Normalization
- Swish Activation
- MaxPooling2D
- Dropout (0.25)

### Classification Head

- Flatten
- Dropout (0.40)
- Dense (128 neurons)
- Batch Normalization
- Dropout (0.20)
- Softmax Output Layer

---

# 🔄 Residual Skip Connection

The first convolutional block incorporates a **Residual Skip Connection**, inspired by ResNet architectures.

Benefits include:

- Improved gradient flow
- Better feature propagation
- Easier optimization of deeper networks
- Reduced degradation problem
- Faster convergence during training

---

# 📈 Training Accuracy

<p align="center">
<img src="images/accuracy_curve.png" width="750">
</p>

---

# 📉 Training Loss

<p align="center">
<img src="images/loss_curve.png" width="750">
</p>

---


# 📊 Final Results

| Metric | Value |
|---------|------:|
| Training Accuracy | **99.97%** |
| Validation Accuracy | **94.11%** |
| Test Accuracy | **89.13%** |
| Test Loss | **0.6001** |

---

# 🧮 Model Summary

| Property | Value |
|----------|-------|
| Classes | 4 |
| Total Parameters | 13,124,868 |
| Trainable Parameters | 13,124,100 |
| Non-trainable Parameters | 768 |
| Model Size | 50.07 MB |

---

# ✨ Key Features

- Custom CNN built entirely from scratch.
- Residual Skip Connections.
- Swish activation function.
- Batch Normalization.
- L2 Regularization.
- Dropout Regularization.
- He Normal weight initialization.
- Residual learning for improved optimization.
- TensorFlow/Keras implementation.
- Medical image classification.

---

# 📝 Training Configuration

| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy *(or Sparse Categorical Crossentropy if used)* |
| Activation | Swish |
| Output Activation | Softmax |
| Regularization | L2 (1e-5) |
| Pooling | MaxPooling2D |
| Dense Layer | 128 |
| Dropout | 0.20 / 0.25 / 0.40 |

---

# 🏥 Applications

This model can be applied to:

- Computer-Aided Diagnosis (CAD)
- Brain MRI Classification
- Medical Image Analysis
- Clinical Decision Support
- AI-assisted Radiology
- Medical Research
- Healthcare AI
- Educational Deep Learning Projects

---

# 📌 Conclusion

This project demonstrates the development of a **Custom Convolutional Neural Network (CNN)** enhanced with **Residual Skip Connections** for multiclass brain tumor MRI classification.

By integrating:

- Residual Learning
- Swish Activation
- Batch Normalization
- L2 Regularization
- Dropout

the model effectively learns discriminative MRI features and achieves **89.13% test accuracy**. This project highlights the design of custom deep learning architectures for medical imaging without relying on pretrained models.

---

## ⭐ If you found this project useful, consider giving it a star!
