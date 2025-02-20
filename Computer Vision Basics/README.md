# 📌 Image Processing and Computer Vision Basics

A Python-based repository for fundamental **image processing** and **computer vision** techniques. This repository covers key operations such as **image representation, transformations, filtering, feature extraction, and visualization**, using libraries like OpenCV, NumPy, and PIL.

## ✨ Core Concepts  

### 1️⃣ Image Representation & Manipulation  
Images in **computer vision** are stored as **arrays of pixel values**. This repository covers:
- **Loading images** using OpenCV, PIL, and Matplotlib.
- **Accessing pixel values** (RGB/BGR representations).
- **Modifying images** (color changes, drawing shapes).
- **Resizing images** using interpolation techniques (nearest-neighbor, bilinear, bicubic).

### 2️⃣ Image Filtering & Enhancement  
**Filtering** is crucial for improving image quality and extracting important details:
- **Noise Reduction** using Gaussian, Median, and Bilateral filters.
- **Sharpening** using convolution operations.
- **Edge Detection** using Sobel, Prewitt, and Canny filters.

### 3️⃣ Feature Extraction & Visualization  
Feature extraction helps identify **patterns and structures** in an image:
- **Histogram Analysis**: Understanding pixel intensity distributions.
- **Color Space Conversions**: Converting images to **grayscale, HSV, LAB** for different processing needs.

### 4️⃣ Image Reading & Writing  
This repository covers multiple methods to **load, display, and save images**:
- **Using OpenCV (`cv2.imread()` and `cv2.imwrite()`)**
- **Using PIL (`Image.open()` and `Image.save()`)**
- **Using Matplotlib (`plt.imread()` and `plt.imshow()`)**

### 5️⃣ Image Statistics & Histograms  
Histograms provide a graphical representation of pixel intensities:
- **Grayscale image histograms** (single-channel intensity distribution).
- **Color histograms** (separate R, G, B distributions).
- **Cumulative distribution functions (CDFs)** to adjust contrast.

### 6️⃣ Image Transformations  
Transforming an image allows manipulation for better analysis:
- **Geometric transformations** (scaling, rotating, flipping).
- **Affine transformations** (translation, shearing, warping).
- **Perspective transformation** (removing distortions).

### 7️⃣ Grayscale & Color Conversions  
Color models are used to represent images differently for various tasks:
- **Grayscale conversion (`cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)`)**
- **HSV & LAB color spaces for better color-based filtering**
- **Thresholding techniques for binarization**

---

## 🚀 Getting Started  

### 🔧 Installation  

Clone this repository and install dependencies:

```bash
git clone https://github.com/Bushra-Butt-17/image-processing-basics.git
cd image-processing-basics
pip install -r requirements.txt
```

### ▶ Running Scripts  

Execute individual scripts to explore different functions Or run the main script to test all functions together.


### 📊 Running Jupyter Notebooks  

For interactive learning, use Jupyter Notebook:

```bash
jupyter notebook
```

Then open notebooks from the **notebooks/** directory.  

---

## 🛠 Dependencies  

This repository requires the following Python libraries:

```txt
opencv-python  
numpy  
matplotlib  
Pillow  
scikit-image  
```

To install, run:

```bash
pip install opencv-python numpy matplotlib Pillow scikit-image  
```

---

## 📜 License  

This project is licensed under the **MIT License**. Feel free to use and modify it as needed.  

---

## 🤝 Contributing  

Contributions are welcome! You can:
- Open an issue for suggestions.
- Submit a pull request with improvements.

---

## 📧 Contact  

For any inquiries, contact **Bushra Butt** via:
📩 Email: [bsdsf21m020@pucit.edu.pk](mailto:bsdsf21m020@pucit.edu.pk)  
📌 GitHub: [Bushra-Butt-17](https://github.com/Bushra-Butt-17)  

---

