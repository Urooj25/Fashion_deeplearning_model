# Fashion Item Classifier 👗👟

A Deep Learning project built with **TensorFlow** and **Keras** to classify fashion items from the **Fashion-MNIST dataset**. This project demonstrates the full machine learning workflow: from model training to real-world testing and advanced image preprocessing.

## 🚀 The Challenge
During testing with real-world photos, the model initially struggled to distinguish between complex shapes (like sneakers and bags) due to the limitations of **Dense Layers** in handling spatial variance. Through iterative debugging and advanced preprocessing, I successfully improved the model's prediction accuracy for custom inputs.

## 🛠️ Tech Stack
* **Framework:** TensorFlow / Keras
* **Language:** Python
* **Libraries:** NumPy (Data manipulation), Matplotlib (Visualization), PIL/Pillow (Image Processing)
* **Environment:** Google Colab

## 🧠 Model Architecture
The model uses a **Sequential Neural Network** approach:
* **Input Layer:** Flatten layer to convert 28x28 images into a 1D array.
* **Hidden Layers:** Multiple Dense layers with ReLU activation for feature learning.
* **Output Layer:** Dense layer with Softmax activation to classify 10 distinct fashion categories.

## 📊 Key Features & Preprocessing
To bridge the gap between "perfect" dataset images and "noisy" real-world photos, I implemented a robust preprocessing pipeline:
* **Grayscale Conversion:** Ensuring compatibility with the single-channel training data.
* **Thresholding & Contrast:** Enhancing object edges to prevent "Bag/T-shirt" misclassification.
* **Strategic Resizing:** Using `thumbnail` and padding techniques to center-align objects within a 28x28 frame.
* **Inversion Logic:** Automatically adjusting background-to-foreground contrast for optimal detection.

## 📈 Results
* **Test Accuracy:** Achieved **~88% accuracy** on the Fashion-MNIST test set.
* **Real-World Testing:** Successfully classified custom images of T-shirts and Footwear after optimizing the preprocessing pipeline.

## 📁 Repository Structure
* `Fashion_Classifier.ipynb`: The main notebook containing training and prediction code.
* `model_weights/`: Saved weights for the trained model.
* `examples/`: Sample images used for testing "The Bug" vs "The Fix" scenarios.

---

### 💡 Learnings
This project was a deep dive into **Spatial Invariance** and why **Convolutional Neural Networks (CNNs)** are often preferred over standard Dense Networks for image tasks. It taught me that in AI, data preparation is just as critical as the model architecture itself.

---

*Feel free to star ⭐ this repository if you found it helpful!*
