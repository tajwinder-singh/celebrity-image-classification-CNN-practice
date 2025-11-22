# Celebrity Image Classification using CNN

https://github.com/user-attachments/assets/5db9bcd9-db46-4c6d-a0ac-c3c81c6868e3


## Overview  
This project focuses on classifying **celebrity images** using a **Convolutional Neural Network (CNN)**.  
It demonstrates the complete deep learning workflow — from data cleaning and preprocessing to model building and hyperparameter tuning.

---

## Steps Followed  

### 1. Image Collection & Cleaning  
- Loaded celebrity images from folders.  
- Handled corrupted or invalid images (`None` returns).  
- Converted images to grayscale or RGB format as needed.

### 2. Face Cropping & Saving  
- Cropped detected faces and saved each with a **unique filename** (original name + number).  
- Ensured proper folder structure for each celebrity category.

### 3. Data Preprocessing  
- Applied `ImageDataGenerator` for data augmentation (rotation, rescaling, etc.).  
- Increased dataset diversity to minimize overfitting.

### 4. Model Building (CNN)  
- Designed a CNN using TensorFlow/Keras.  
- Included layers: convolution, pooling, flattening, and dense.  

### 5. Model Training  
- Trained the CNN on augmented datasets.  
- Computed **class weights** to handle data imbalance.

### 6. Hyperparameter Tuning (Bayesian Optimization)  
- Tuned learning rate, dropout, filters, and dense units.  
- Applied the following rule of thumb for number of trials:  
  - Small range → `n × 10` trials  
  - Medium range → `n × 12` trials  
  - Wide range → `100+` trials or reduce parameter ranges.

---

## Learnings  
- Focus on *what* a function does instead of *how* it works internally.  
- Maintain a consistent and modular project structure for reusability.  
- Image augmentation enhances model generalization.  
- Bayesian Optimization is efficient for fine-tuning hyperparameters.

---

## Note  
Use the cropped dataset directly to train the model as I was unable to uplaod the raw data because it was too big.

Model training for full epochs was skipped to save time — the goal was to focus on building a **correct and reusable pipeline**.

---




## Tech Stack  
- Python  
- TensorFlow / Keras  
- NumPy, Pandas, Matplotlib  
- OpenCV  

