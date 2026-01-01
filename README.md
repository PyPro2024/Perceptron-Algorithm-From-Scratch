# Perceptron Algorithm: Implementation from Scratch

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![NumPy](https://img.shields.io/badge/NumPy-Math-013243?style=flat&logo=numpy)

##  Project Overview
This project involves building a **Single-Layer Perceptron**—the fundamental building block of Artificial Neural Networks—entirely from scratch using **Python** and **NumPy**.

Instead of using high-level API calls (like `keras.layers.Dense`), this repository manually implements the mathematical logic for:
1.  **Weighted Sum Calculation** (Dot Product).
2.  **Activation Function** (Step Function).
3.  **Weight Update Rule** (Rosenblatt's Learning Algorithm).

##  Mathematical Logic
The Perceptron makes a prediction based on linear combinations of input features:



* **Activation:** The model uses a Heaviside Step Function: output is `1` if $z \ge 0$, else `-1`.
* **Learning Rule:** Weights are updated iteratively based on the error:
    $$w := w + \Delta w$$
    $$\Delta w = \eta \times (target - prediction) \times x_i$$
    *(Where $\eta$ is the learning rate)*

## Tech Stack
* **Language:** Python
* **Core Logic:** NumPy (for vectorization and efficiency)
* **Data Processing:** Pandas
* **Dataset:** Iris Dataset (Binary Classification: *Iris-setosa* vs. *Others*)

##  Code Structure
The implementation is encapsulated in a `Perceptron` class with the following methods:
* `__init__`: Initializes learning rate and epochs.
* `fit(X, y)`: Trains the model by iterating through the dataset and updating weights.
* `net_input(X)`: Calculates the dot product $w \cdot x + b$.
* `predict(X)`: Applies the step function to return class labels.

##  How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/PyPro2024/Perceptron-Algorithm-From-Scratch.git]
    ```
2.  **Install dependencies:**
    ```bash
    pip install numpy pandas scikit-learn
    ```
3.  **Run the Notebook:**
    Open `Perceptron.ipynb` in Jupyter Notebook or Google Colab to see the training process and accuracy results.

##  Results
* **Training:** The model successfully converges and learns to separate the linearly separable classes of the Iris dataset.
* **Accuracy:** Achieved **100% accuracy** on the test set for this specific binary classification task.

---
*If you find this foundational project helpful, feel free to ⭐ the repo!*
