# 📌 HOG Vision Classifier

## 🖼️ Histogram of Oriented Gradients (HOG) Overview
Histogram of Oriented Gradients (HOG) is a **feature descriptor** used primarily for object detection and image classification. It captures the **gradient structure** of an image, emphasizing the edges and shapes, which are crucial for recognizing objects.

HOG is widely used in **computer vision** for applications such as **pedestrian detection, facial recognition, and handwritten digit classification**.

---

## 🏗️ How HOG Works
The core idea of HOG is to represent an image based on its **gradient orientations** rather than raw pixel values. This helps in making the model robust against changes in illumination and small geometric transformations.

### 🔹 Step 1: Preprocessing
- Convert the image to **grayscale** (if it's in color) to reduce computational complexity.
- Optionally, normalize the image for **lighting and contrast adjustments**.

### 🔹 Step 2: Compute Gradients
- Compute the **gradient magnitude and direction** for each pixel using **Sobel filters**.
- This step highlights the **edges** in the image where intensity changes occur.

### 🔹 Step 3: Divide into Cells
- The image is divided into small **cells** (e.g., 8x8 or 16x16 pixels).
- Gradients are **binned** based on their orientation (e.g., 0° to 180° divided into 9 bins).

### 🔹 Step 4: Block Normalization
- Multiple cells are grouped into **blocks** (e.g., 2x2 cells) to perform **local contrast normalization**.
- This step helps in making the features **scale-invariant**.

### 🔹 Step 5: Feature Vector Construction
- The HOG descriptor is formed by concatenating **histograms of gradient orientations** from all cells.
- This **feature vector** is then used for training a classifier (e.g., SVM, Decision Trees, or Deep Learning models).

---

## 🏆 Applications of HOG
HOG features are widely used in various **computer vision tasks**, including:

1. **🚶 Pedestrian Detection** → Used in self-driving cars and surveillance systems.
2. **👤 Face Recognition** → Early face detectors like **Dlib’s face detector** use HOG.
3. **🔢 Handwritten Digit Recognition** → Used in OCR (Optical Character Recognition).
4. **📦 Object Detection** → Vehicles, animals, and other objects in images/videos.

---

## 🛠️ Implementation Guide
### 📌 Installing Dependencies
To implement HOG-based classification, install the necessary Python libraries:
```bash
pip install numpy opencv-python scikit-learn matplotlib
```

### 📌 Code Example: Extracting HOG Features
```python
import cv2
import numpy as np
from skimage.feature import hog
import matplotlib.pyplot as plt

# Load Image
def load_image(image_path):
    img = cv2.imread(image_path, cv2.IMREAD_GRAYSCALE)
    return img

# Extract HOG Features
def extract_hog_features(image):
    features, hog_image = hog(image, pixels_per_cell=(8, 8), cells_per_block=(2, 2),
                              orientations=9, visualize=True, block_norm='L2-Hys')
    return features, hog_image

# Display HOG Features
def visualize_hog(image_path):
    image = load_image(image_path)
    features, hog_image = extract_hog_features(image)
    
    fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(10, 5))
    ax1.imshow(image, cmap='gray')
    ax1.set_title("Original Image")
    ax2.imshow(hog_image, cmap='gray')
    ax2.set_title("HOG Features")
    plt.show()

# Run visualization
visualize_hog('sample_image.jpg')
```

### 📌 Training a Classifier with HOG Features
Once HOG features are extracted, they can be used to train a machine learning classifier such as **Support Vector Machines (SVM), Decision Trees, or Neural Networks**.

Example using **SVM**:
```python
from sklearn.svm import SVC
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

# Load dataset (example with pre-extracted HOG features)
X_train, X_test, y_train, y_test = train_test_split(feature_vectors, labels, test_size=0.2, random_state=42)

# Train an SVM classifier
classifier = SVC(kernel='linear')
classifier.fit(X_train, y_train)

# Test on unseen data
y_pred = classifier.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print(f"Model Accuracy: {accuracy * 100:.2f}%")
```

---

## 📊 Key Advantages of HOG
✅ **Illumination Invariance** → Works well in different lighting conditions.  
✅ **Geometric Robustness** → Effective even with slight translations and rotations.  
✅ **Computational Efficiency** → Faster than deep learning for simple tasks.  
✅ **Effective for Object Detection** → Used in classic pedestrian and face detection models.  

---

## 📜 License
This project is licensed under the **MIT License**. Feel free to use and modify it as needed.

---

## 🤝 Contributing
Contributions are welcome! You can:
- Open an **issue** for suggestions.
- Submit a **pull request** with improvements.

---

## 📧 Contact
For any inquiries, contact **Bushra Butt** via:  
📩 **Email**: bsdsf21m020@pucit.edu.pk  
📌 **GitHub**: [Bushra-Butt-17](https://github.com/Bushra-Butt-17)  

---

**🔹 Happy Coding! 🚀**

