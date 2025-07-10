
#  Multimodal Housing Price Prediction

##  Objective

The goal of this task was to predict house prices using **multimodal machine learning**, combining **tabular data** (like square footage, quality, neighborhood) with **visual data** (house images). This approach aims to improve prediction performance by utilizing both structured and unstructured features.

---

##  Methodology / Approach

1. **Dataset Used**:
   - **Ames Housing Dataset** for tabular features.
   - **House Rooms & Streets Image Dataset** (from Kaggle) for visual features.

2. **Preprocessing**:
   - Tabular features were encoded and scaled using `LabelEncoder` and `StandardScaler`.
   - Images were loaded, resized to (128x128), and normalized.

3. **Model Architecture**:
   - **CNN branch** for image input: Two Conv2D + MaxPooling layers followed by flattening.
   - **Dense branch** for tabular input: Two Dense layers.
   - **Fusion**: Concatenation of CNN and tabular outputs, followed by final Dense layers for regression.

4. **Training**:
   - Combined model trained for 2 epochs due to time/computational constraints.
   - Loss function: `Mean Squared Error (MSE)`
   - Evaluation metrics: `Mean Absolute Error (MAE)` and `Root Mean Squared Error (RMSE)`

---

##  Key Results / Observations

- **MAE (Test Set)**: ≈ 78,417  
- **RMSE (Test Set)**: ≈ 101,169
- **Observation**:
   - Validation MAE decreased with each epoch, showing the model was learning.
   - Performance may improve further with more epochs and better hyperparameter tuning.
   - Using both image and tabular data (multimodal learning) allows capturing more complex patterns than using either alone.

---

##  Skills Demonstrated

- Convolutional Neural Networks (CNNs)
- Feature fusion from multiple data modalities
- Data preprocessing and normalization
- Regression modeling and evaluation
- Building custom models using TensorFlow/Keras
