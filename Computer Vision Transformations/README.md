# Image Processing with OpenCV

## 📌 Overview
This project explores fundamental image processing operations using OpenCV. It covers grayscale conversion, arithmetic and logical operations, flipping, rotations, concatenation, and video capture. The tasks demonstrate how images can be manipulated for different applications in computer vision.

---

## 📷 Task 1: Grayscale Conversion and Arithmetic Operations
### 🔹 Original vs. Processed Image
The original image is loaded in color and then converted to grayscale. Several arithmetic operations are applied to modify brightness and contrast:

- **Grayscale Conversion**: Removes color, focusing only on light and dark areas.
- **Brightness Adjustments**:
  - Adding **90**: Makes the image brighter.
  - Subtracting **90**: Makes the image darker.
- **Contrast Adjustments**:
  - Multiplying by **1.5**: Increases contrast, making bright areas brighter and dark areas darker.
- **Image Inversion**: Converts bright pixels to dark and vice versa.

📌 **Observation**: These operations change how an image appears by adjusting brightness and contrast, helping highlight different features.

---

## 🔢 Task 2: Arithmetic and Logical Operations on Two Images
### 🖼 Input Images
We use two grayscale images for this task.

### 🔹 Arithmetic Operations
1. **Addition**: Blends two images together, brightening overlapping areas.
2. **Subtraction**: Highlights differences by making similar regions dark and differences bright.
3. **Multiplication**: Enhances contrast in overlapping bright regions.

### 🔹 Logical Operations
1. **Bitwise AND**: Retains only overlapping bright areas.
2. **Bitwise OR**: Combines bright areas from both images.
3. **Bitwise XOR**: Highlights differences between the two images.
4. **Bitwise NOT**: Inverts pixel values, creating a negative of the image.

📌 **Observation**: Arithmetic operations blend and adjust brightness, while logical operations emphasize similarities and differences.

---

## 📷 Task 3: Capturing and Saving an Image via Webcam
A webcam is used to capture a real-time image and save it.

📌 **Implementation**:
- The program opens the webcam.
- Displays the live video stream.
- Captures and saves an image as "DIP.jpg" when 'q' is pressed.

📌 **Observation**: This task enables real-time image processing applications such as face recognition.

---

## 🔄 Task 4: Image Flipping
### 🔹 Types of Flipping
1. **Vertical Flip**: Turns the image upside down.
2. **Horizontal Flip**: Creates a mirror image by swapping the left and right sides.
3. **Both Axes Flip**: Rotates the image 180 degrees.

📌 **Observation**: Flipping is useful in data augmentation for machine learning models.

---

## ⏳ Task 5: Image Rotation
### 🔹 Types of Rotation
1. **90° Clockwise**: Moves the top to the right.
2. **180° Rotation**: Flips the image upside down.
3. **270° Clockwise**: Moves the top to the left.

📌 **Observation**: Rotation changes an image’s orientation, useful in medical imaging and object detection.

---

## 🔗 Task 6: Concatenation of Images
### 🔹 Concatenation Types
1. **Original & Flipped Images**: Displays transformations side-by-side.
2. **Original & Rotated Images**: Shows rotational transformations.

📌 **Observation**: Concatenation is useful for comparative analysis and dataset preparation.

---

## 🎥 Task 7: Image and Video Reading
- Displays an image of cats.
- Reads and plays a video (dog.mp4) frame by frame.
- Stops playback when 'd' is pressed.

📌 **Observation**: Understanding video frames is essential for real-time applications like motion detection.

---

## 🛠️ OpenCV Functions Used
| Operation | OpenCV Function |
|-----------|----------------|
| Flipping | `cv2.flip(image, value)` |
| Rotation | `cv2.rotate(image, mode)` |
| Concatenation | `cv2.hconcat(), cv2.vconcat()` |
| Addition | `cv2.addWeighted(img1, wt1, img2, wt2, gamma)` |
| Subtraction | `cv2.subtract(img1, img2)` |
| Bitwise AND | `cv2.bitwise_and(img1, img2)` |
| Bitwise OR | `cv2.bitwise_or(img1, img2)` |
| Bitwise XOR | `cv2.bitwise_xor(img1, img2)` |
| Bitwise NOT | `cv2.bitwise_not(img1)` |

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
- 📩 **Email**: bsdsf21m020@pucit.edu.pk
- 📌 **GitHub**: [Bushra-Butt-17](https://github.com/Bushra-Butt-17)

