
# 📄 About `plant_.py`

The `plant_.py` file is a Python script designed to detect and classify **plant leaf diseases** using **Convolutional Neural Networks (CNNs)** in **TensorFlow**. It appears to be originally written and exported from Google Colab.

## 🔍 Purpose:
To build, train, evaluate, and visualize a deep learning model that can classify different types of plant diseases from leaf images.

## 🔧 Key Functionalities:

1. **Google Drive Integration:**
   - Automatically mounts Google Drive to access the dataset.

2. **Data Loading:**
   - Loads images using `image_dataset_from_directory` with a **train-validation split**.
   - Applies label encoding as `categorical` for multi-class classification.

3. **Data Augmentation & Preprocessing:**
   - Includes horizontal flips, zooms, and rotations for better generalization.
   - Normalizes pixel values (rescaling to [0,1]).

4. **Model Architecture:**
   - A deep CNN with:
     - 5 Convolutional layers (32 → 512 filters)
     - MaxPooling after each conv layer
     - Dense layer + Dropout for regularization
     - Final softmax layer for classification

5. **Training:**
   - Uses Adam optimizer and trains for 40 epochs.
   - Tracks and prints training/validation accuracy.

6. **Evaluation:**
   - Computes predictions on validation data.
   - Prints a **classification report**.
   - Displays:
     - Accuracy/Loss plots
     - Confusion matrix
     - ROC curve (micro-averaged AUC)

7. **Statistical Analysis:**
   - Performs:
     - **Z-Test**
     - **Paired T-Test**
     - **Levene’s Test** for variance comparison
   - Useful for checking consistency of predictions.

## 🧠 Libraries Used:
- TensorFlow / Keras
- Matplotlib, Seaborn (visualization)
- Scikit-learn (metrics, tests)
- NumPy, SciPy
- Google Colab utilities

## 📌 Notes:
- The script is **modular** and can be run end-to-end in **Google Colab**.
- You should modify `dataset_path` to match your dataset location if running outside Colab.
- Statistical tests provide deeper insights but are optional for general use.
