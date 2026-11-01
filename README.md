# EXP. 6 – EDGE DETECTION USING OPENCV

## NAME:  NIKILA D  
## REG NO: 212224230187

## Aim

To implement different edge detection techniques using OpenCV and Python to identify edges and boundaries in an image.

## Software Requirements

- Python
- Anaconda
- Jupyter Notebook
- OpenCV
- NumPy
- Matplotlib

## Edge Detection Techniques

1. Sobel Edge Detection
2. Laplacian Edge Detection
3. Canny Edge Detection

## Algorithm

1. Import the required libraries: OpenCV, NumPy, and Matplotlib.
2. Read the input image using `cv2.imread()`.
3. Convert the input image into grayscale.
4. Display the original image.
5. Apply Sobel edge detection in horizontal and vertical directions.
6. Combine both Sobel gradients using `cv2.magnitude()`.
7. Apply Laplacian edge detection using `cv2.Laplacian()`.
8. Apply Canny edge detection using `cv2.Canny()`.
9. Display all the edge-detected images separately.
10. Compare the results of different edge detection techniques.

## Implementation

### 1. Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### 2. Read and Convert the Image

```python
image = cv2.imread('Image.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```

### 3. Display Original Image

```python
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

## OUTPUT:
<img width="512" height="581" alt="image" src="https://github.com/user-attachments/assets/c22dec29-3a4e-412f-99e3-0069bcf59d69" />

### 4. Sobel Edge Detection

```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)

sobel_combined = cv2.magnitude(sobel_x, sobel_y)

plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

## OUTPUT:
<img width="577" height="552" alt="image" src="https://github.com/user-attachments/assets/92b93aef-d37c-4f1f-b7b1-df241b1c2e0a" />

### 5. Laplacian Edge Detection

```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)

plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

## OUTPUT;
<img width="580" height="557" alt="image" src="https://github.com/user-attachments/assets/542b0c34-d982-42e1-85b8-748fad4692ee" />

### 6. Canny Edge Detection

```python
canny_edges = cv2.Canny(gray_image, 50, 150)

plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

## Output:
<img width="520" height="561" alt="image" src="https://github.com/user-attachments/assets/ff5ab902-471c-48ef-8c08-c07301feb4f7" />

## Result

Thus, Sobel, Laplacian, and Canny edge detection techniques were successfully implemented using OpenCV and Python. Each technique detects image edges differently and helps identify important boundaries and features.

