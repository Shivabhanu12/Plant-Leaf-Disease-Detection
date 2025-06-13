
# 🌿 Plant Leaf Disease Detection

This project uses a Convolutional Neural Network (CNN) to detect and classify plant leaf diseases from images. It is built using TensorFlow and trained on a dataset of labeled leaf images.

## 📁 Dataset
- **Path**: Google Drive – `https://drive.google.com/drive/folders/1pGoT3TOhDvFWUDSV_7QZrjjw-JqPU8pD?usp=sharing`
- **Format**: Directory structure with subfolders for each class (disease category).
- **Split**: Automatically split into training and validation sets (80/20).

## 🧠 Model Architecture
- **Input Shape**: 128x128 RGB images
- **Layers**:
  - 5× `Conv2D` + `MaxPooling2D`
  - `Flatten` → `Dense(128)` → `Dropout(0.5)`
  - Output: `Dense(Softmax)` with units = number of classes
- **Activation**: ReLU (Hidden), Softmax (Output)
- **Optimizer**: Adam (`lr = 0.001`)
- **Loss**: Categorical Crossentropy

## 🔄 Data Augmentation
Applied to the training data:
- Horizontal Flip
- Random Rotation (20%)
- Random Zoom (20%)

Validation data is only rescaled.

## 📊 Evaluation Metrics
- Accuracy (Training & Validation)
- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)
- ROC Curve (Micro-averaged AUC)
- Type I & II Error (if binary)
- Statistical Tests:
  - Z-test
  - Paired T-test
  - Levene's Variance Test

## 🛠️ Requirements
```bash
pip install tensorflow matplotlib seaborn scikit-learn
```

## ▶️ How to Run
1. Upload your dataset to Google Drive.
2. Mount the drive in Colab:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
3. Run the code (`plant_.py`) in Google Colab or Jupyter.
4. Modify `dataset_path` to point to your dataset location.

## 📈 Results
- **Train Accuracy**: ~Your final value
- **Validation Accuracy**: ~Your final value
- Visualized:
  - Learning curves
  - Confusion matrix
  - ROC curve

## 🧪 Notes
- Works for multi-class classification.
- For binary classification, Type I and II errors are also shown.
- Statistical tests validate prediction distribution differences.

## 📬 Author
**Konde Shiva Bhanu** – B.Tech CSE (Data Science)  
SR University | 2022–2026
