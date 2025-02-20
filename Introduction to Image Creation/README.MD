# 📌 Image Processing with Python

Welcome to **Image Processing with Python**! 🎨 This repository contains **various image manipulation techniques** implemented in Python using **NumPy, OpenCV, and Matplotlib**.

## 📜 Overview

This repository focuses on fundamental image generation and transformation techniques:

- ✅ Creating images with geometric shapes
- ✅ Drawing grids and patterns
- ✅ Mirroring images
- ✅ Understanding image manipulation with OpenCV & NumPy

Each method provides an interactive approach to **customizing images** using user-defined parameters like **image size, line thickness, and box size**.

---

## 🚀 Getting Started

### 🔧 Prerequisites

Ensure you have Python installed along with the following libraries:

```sh
pip install numpy opencv-python matplotlib
```

### 📂 Clone the Repository

```sh
git clone https://github.com/Bushra-Butt-17/image-processing-python.git
cd image-processing-python
```

---

## 🖼️ Image 1: Black Square with White Inner Square

### 📝 Description

This function **creates an image with a black background and a white inner square** placed at the center.

### 🖥️ Code Example

```python
import numpy as np
import matplotlib.pyplot as plt

def create_image_with_square(image_size, box_size):
    image = np.zeros((image_size, image_size, 3), dtype=np.uint8)
    start = (image_size - box_size) // 2
    end = start + box_size
    image[start:end, start:end] = [255, 255, 255]
    plt.imshow(image)
    plt.axis('off')
    plt.show()
```

### 📌 Output

---

## 🖼️ Image 2: Four Small Black Squares in Corners

### 📝 Description

This function generates an image with **four black squares at each corner** of a white canvas.

### 🖥️ Code Example

```python
def create_image_with_four_boxes(image_size, box_size):
    image = np.ones((image_size, image_size, 3), dtype=np.uint8) * 255
    image[:box_size, :box_size] = [0, 0, 0]
    image[:box_size, -box_size:] = [0, 0, 0]
    image[-box_size:, :box_size] = [0, 0, 0]
    image[-box_size:, -box_size:] = [0, 0, 0]
    plt.imshow(image)
    plt.axis('off')
    plt.show()
```

### 📌 Output

---

## 🖼️ Image 3: Grid of Lines

### 📝 Description

This function **creates an image with a grid of horizontal and vertical black lines**.

### 🖥️ Code Example

```python
def create_grid(image_size, num_lines, line_thickness):
    image = np.ones((image_size, image_size, 3), dtype=np.uint8) * 255
    for i in range(num_lines):
        y = (i + 1) * (image_size // (num_lines + 1))
        image[y:y + line_thickness, :] = [0, 0, 0]
    for i in range(num_lines):
        x = (i + 1) * (image_size // (num_lines + 1))
        image[:, x:x + line_thickness] = [0, 0, 0]
    plt.imshow(image)
    plt.axis('off')
    plt.show()
```

### 📌 Output

---

## 🖼️ Image 4: Colored Boxes in Corners

### 📝 Description

This function generates a white canvas with **four colored boxes** placed at each corner: black, blue, green, and red.

### 🖥️ Code Example

```python
def create_colored_corners(image_size):
    image = np.ones((image_size, image_size, 3), dtype=np.uint8) * 255
    box_size = image_size // 10
    image[:box_size, :box_size] = [0, 0, 0]
    image[:box_size, -box_size:] = [255, 0, 0]
    image[-box_size:, :box_size] = [0, 255, 0]
    image[-box_size:, -box_size:] = [0, 0, 255]
    plt.imshow(image)
    plt.show()
```

### 📌 Output

---

## 🖼️ Image 5: Mirroring the Lower Half of an Image

### 📝 Description

This function reads an image, converts it to **grayscale**, and mirrors its **lower half** to replace the **upper half**.

### 🖥️ Code Example

```python
import cv2

def mirror_image(image_path, output_path):
    image = cv2.imread(image_path)
    gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
    height, width = gray_image.shape
    lower_half = gray_image[height//2:, :]
    mirrored_half = cv2.flip(lower_half, 0)
    mirrored_image = gray_image.copy()
    mirrored_image[:height//2, :] = mirrored_half
    cv2.imwrite(output_path, mirrored_image)
```

### 📌 Output

---

## 📚 Learning Outcomes

By working with this repository, you will:

✅ Understand image manipulation with **NumPy and OpenCV**\
✅ Learn to **process pixel values** for transformations\
✅ Visualize images using **Matplotlib**\
✅ Gain **hands-on experience** in **basic computer vision techniques**

---

## 🏆 Contributing

Have an idea to enhance this repository? Feel free to contribute! Follow these steps:

1. **Fork** this repository 🍴
2. **Clone** the repository to your local machine 🖥️
3. Create a **new branch** and make modifications ✏️
4. **Push** the changes and submit a **Pull Request** 🔄

---

## 🔗 Resources

- [NumPy Documentation](https://numpy.org/doc/)
- [OpenCV Documentation](https://docs.opencv.org/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)

---

## 📩 Contact

For any queries, feel free to reach out at **bsdsf21m020\@pucit.edu.pk 📧**

🎯 **Happy Coding!** 🚀


