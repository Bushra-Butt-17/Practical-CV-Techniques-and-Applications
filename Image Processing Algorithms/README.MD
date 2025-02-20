# 📌 Image Processing Algorithms

A Python-based implementation of fundamental image processing techniques including resizing, convolution, and filtering.

---

## ✨ Features

- **📏 Resizing Algorithms:**
  - Nearest Neighbor Interpolation 🟩
  - Bilinear Interpolation 🔵
- **🎨 Image Filtering:**
  - Gaussian Blur 🟡
  - Edge Detection using Convolution 🔴

---

## 🔬 Implemented Algorithms

### 1️⃣ Nearest Neighbor Resizing

✅ **Description:**
Nearest neighbor interpolation is a simple and fast image resizing technique. It selects the closest pixel from the original image to fill in the resized image, without considering any interpolation or averaging.

📌 **Key Points:**
- Fastest resizing method.
- Produces blocky and pixelated images when enlarging.
- Ideal for applications where speed is more important than quality.

🖼️ **Example Output:**
*(Image illustrating nearest neighbor resizing output)*

---

### 2️⃣ Bilinear Interpolation

✅ **Description:**
Bilinear interpolation uses the closest **four pixels** to estimate new pixel values. This results in a smoother and less pixelated image compared to nearest neighbor interpolation.

📌 **Key Points:**
- Uses weighted averages of surrounding pixels.
- Produces smoother images compared to nearest neighbor.
- Slightly more computationally expensive than nearest neighbor.

🖼️ **Example Output:**
*(Image illustrating bilinear interpolation output)*

---

### 3️⃣ Gaussian Filtering

✅ **Description:**
Gaussian filtering applies a **Gaussian kernel** to blur the image, reducing noise and detail. This is widely used in image pre-processing for tasks like edge detection and smoothing.

📌 **Key Points:**
- Reduces noise and detail in images.
- Uses a Gaussian function to determine weights for each pixel.
- Helps in tasks like edge detection and image segmentation.

🖼️ **Example Output:**
*(Image illustrating Gaussian filtering output)*

---

### 4️⃣ Convolution (Edge Detection)

✅ **Description:**
Convolution is used for edge detection by applying a **Laplacian kernel** (or other kernels) to highlight sharp intensity changes in an image.

📌 **Key Points:**
- Enhances edges and boundaries in an image.
- Uses a predefined kernel (such as Sobel or Laplacian).
- Helps in object detection and feature extraction.

🖼️ **Example Output:**
*(Image illustrating edge detection output)*

---

## 🚀 How to Run

1️⃣ Clone the repository:

```bash
git clone https://github.com/Bushra-Butt-17/image-processing-algorithms.git
cd image-processing-algorithms
```

2️⃣ Install dependencies:

```bash
pip install -r requirements.txt
```

3️⃣ Run the script:

```bash
python main.py
```

---

## 📜 License

This project is licensed under the **MIT License**. Feel free to use and modify it as needed.

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

---

## 📧 Contact

For any inquiries, contact [ Bushra Shahbaz](mailto\:bsdsf21m020@pucit.edu.pk) or visit the [GitHub Repository](https://github.com/Bushra-Butt-17/image-processing-algorithms).


