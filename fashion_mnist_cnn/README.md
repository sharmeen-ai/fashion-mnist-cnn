# Fashion MNIST Image Classification using CNN

A Convolutional Neural Network (CNN) built with TensorFlow/Keras to classify clothing items from the **Fashion MNIST** dataset into 10 categories — achieving ~91–93% test accuracy.

---

## 📁 Project Structure

```
fashion-mnist-cnn/
│
├── fashion_mnist_cnn.ipynb   # Main Jupyter Notebook (fully commented)
├── fashion_mnist_cnn.h5      # Saved trained model (generated on run)
├── README.md                 # Project documentation
└── requirements.txt          # Python dependencies
```

---

## 📌 About the Dataset

The [Fashion MNIST](https://github.com/zalandoresearch/fashion-mnist) dataset contains **70,000 grayscale images** (28×28 pixels) across 10 clothing categories:

| Label | Class | Label | Class |
|-------|-------|-------|-------|
| 0 | T-shirt/top | 5 | Sandal |
| 1 | Trouser | 6 | Shirt |
| 2 | Pullover | 7 | Sneaker |
| 3 | Dress | 8 | Bag |
| 4 | Coat | 9 | Ankle Boot |

---

## 🧠 Model Architecture

```
Input (28×28×1)
    → Conv2D(32, 3×3, ReLU)       # Detect edges and textures
    → MaxPooling2D(2×2)            # Reduce spatial dimensions
    → Conv2D(64, 3×3, ReLU)       # Detect higher-level patterns
    → MaxPooling2D(2×2)
    → Dropout(0.25)                # Regularization
    → Flatten
    → Dense(128, ReLU)
    → Dropout(0.5)                 # Stronger regularization
    → Dense(10, Softmax)           # Output: 10 class probabilities
```

**Optimizer:** Adam | **Loss:** Sparse Categorical Crossentropy | **Metric:** Accuracy

---

## 📋 Tasks Breakdown

| Task | Description |
|------|-------------|
| Task 1 | Data loading, normalization `[0,1]`, reshaping to `(28,28,1)` |
| Task 2 | CNN architecture design with Conv, Pooling, Dropout layers |
| Task 3 | Training with Early Stopping (patience=3) + training curve plots |
| Task 4 | Evaluation — test accuracy, annotated confusion matrix, classification report |
| Task 5 | Visual predictions with color-coded correct/incorrect labels |

---

## ✅ Key Features

- **Early Stopping** — monitors validation loss, stops training automatically to prevent overfitting
- **Model Saving** — trained model saved as `.h5` for reuse without retraining
- **Annotated Confusion Matrix** — cell values shown for easy interpretation
- **Color-coded Predictions** — green = correct, red = incorrect
- **Clean, commented code** — each decision explained inline

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/fashion-mnist-cnn.git
   cd fashion-mnist-cnn
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Open the notebook**
   ```bash
   jupyter notebook fashion_mnist_cnn.ipynb
   ```

4. Run all cells from top to bottom. The trained model will be saved as `fashion_mnist_cnn.h5`.

---

## 📊 Results

- **Test Accuracy:** ~91–93%
- Training monitored with Early Stopping (patience = 3 epochs)
- Most commonly confused classes: **Shirt** vs **T-shirt/top** (visually similar)

---

## 🛠️ Requirements

- Python 3.8+
- TensorFlow 2.x
- NumPy
- Matplotlib
- scikit-learn

---

## 👤 Author

**Sharmeen Ahsan**  
sharmeens19@gmail.com
