# Fashion-MNIST Classification & Explainability

This project focuses on building a deep learning model to classify images from the Fashion-MNIST dataset and understanding how the model makes its predictions using explainability techniques.

The project was developed as part of a deep learning assignment to explore both image classification and model interpretability.

---

## Dataset

The project uses the Fashion-MNIST dataset, which contains 70,000 grayscale images (28×28 pixels) distributed across 10 clothing categories.

Classes include:

- T-shirt/Top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle Boot

---

## Project Workflow

The notebook follows these main steps:

1. Load the Fashion-MNIST dataset
2. Preprocess the images (normalization and flattening)
3. Build and train a Multi-Layer Perceptron (MLP)
4. Evaluate model performance
5. Visualize predictions
6. Analyze incorrect classifications
7. Explain model predictions using SHAP
8. Interpret the learned features and model behavior

---

## Model Architecture

The implemented model is a simple MLP consisting of:

- Input Layer (784 features)
- Dense Layer (128 neurons, ReLU)
- Dropout Layer
- Dense Layer (64 neurons, ReLU)
- Output Layer (10 neurons, Softmax)

The model is trained using:

- Adam Optimizer
- Sparse Categorical Crossentropy Loss
- Accuracy as the evaluation metric

---

## Results

The notebook includes:

- Model Accuracy
- Confusion Matrix
- Sample Predictions
- Correct vs Incorrect Predictions
- SHAP Explainability Visualizations
- Feature Importance Analysis
- Error Analysis and Model Interpretation

---

## Explainability

To better understand the model's decisions, SHAP (SHapley Additive exPlanations) is used to highlight which image pixels contribute the most to each prediction.

The explanations show that the model mainly relies on:

- Object outlines
- Shape information
- Shoe soles
- Bag handles
- Clothing edges

rather than background pixels.

---

## Observations

Some classes are naturally more difficult to distinguish because of their similar appearance.

The most common confusions are between:

- Shirt and T-shirt/Top
- Pullover and Coat
- Sneaker and Ankle Boot

These errors mainly occur because Fashion-MNIST images are grayscale and have a low resolution (28×28 pixels), making fine details difficult to identify.

---

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SHAP

---

## Repository Structure

```
├── Fashion_MNIST.ipynb
├── README.md
└── requirements.txt (optional)
```

---

## Future Improvements

Possible improvements include:

- Building a CNN model
- Applying Grad-CAM for visual explanations
- Comparing MLP and CNN performance
- Using data augmentation
- Improving overall classification accuracy

---

## Author

This project was completed as part of a Deep Learning assignment to practice image classification and model explainability using the Fashion-MNIST dataset.
