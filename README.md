# COVID-19 Chest X-ray Classification with CNN, VGG19, and DenseNet

This group project focuses on performing a **quantitative comparison** of different deep learning models and preprocessing strategies for classifying chest X-ray images into four categories: **COVID**, **Normal**, **Lung Opacity**, and **Viral Pneumonia**.

The aim was to explore how various preprocessing techniques and model architectures affect classification performance on both multiclass and binary tasks.

## 🎯 Project Goals

- Compare the performance of three models: **Custom CNN**, **VGG19**, and **DenseNet**.
- Analyze how different **image preprocessing methods** influence model accuracy.
- Examine the impact of using a **balanced vs. original dataset**.
- Explore both **4-class classification** and a simplified **binary classification** (COVID vs Non-COVID).

## 📂 Dataset

- Chest X-ray images labeled into:  
  **COVID**, **Normal**, **Lung Opacity**, and **Viral Pneumonia**.
- The dataset was split into **training**, **validation**, and **test** sets.
- A **balanced version** was created and tested, but it showed lower generalization, so the **original dataset was used for main analysis**.

## 🧪 Preprocessing Techniques

Each model was trained on the original dataset with the following image preprocessing variants:

- **CLAHE** (Contrast Limited Adaptive Histogram Equalization)
- **Image Complement**
- **Canny Edge Detection**
- **Lung Masks**

These transformations were applied to evaluate how they affect feature extraction and classification outcomes.

## 🧠 Models Compared

1. **Custom CNN**  
   - Built using Keras from scratch.
   - Used BatchNormalization, Dropout, and Conv2D layers.

2. **VGG19**  
   - Pretrained model from `keras.applications`.
   - Fine-tuned for our dataset.

3. **DenseNet**  
   - Also pretrained and adapted for multiclass output.

All models were trained using the **Adam optimizer** and evaluated using consistent metrics across experiments.

## ⚙️ Training Setup

- **Loss function**: Categorical crossentropy (for 4-class); Binary crossentropy (for COVID vs. Non-COVID).
- **Optimizer**: Adam
- **Train/Validation/Test Split** was applied for each variant.
- Data augmentation and image resizing were included where needed.

## 📊 Evaluation Metrics

To ensure a robust comparison between models and configurations, We used:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC (for binary classification)
- Confusion matrices (to inspect per-class behavior)

These metrics were reported for each experiment to enable clear, quantitative analysis.

## 🧠 Binary Classification

In addition to multiclass classification, We tested **binary classification** where the task was to distinguish **COVID vs Non-COVID** cases. This helped assess model sensitivity to COVID detection alone and provided a different angle for evaluation.

