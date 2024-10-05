# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:

### Developed by: Vikash s
### Register no: 212222240115

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Load the image
```
image = cv2.imread('tortoise .png')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
## Output:

![image](https://github.com/user-attachments/assets/96b18726-9b24-4aca-a32b-8f4439bcf254)

### SOBEL EDGE DETECTOR
```
# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.subplot(2, 2, 2)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
## Output:


![image](https://github.com/user-attachments/assets/8d59798b-0340-438a-80ee-69d9eff638a8)


### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.subplot(2, 2, 3)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')

```
## Output:

![image](https://github.com/user-attachments/assets/002f82ee-a624-4ebf-8ed2-2a6412a1ab15)

### CANNY EDGE DETECTOR
```
# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.subplot(2, 2, 4)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
## Output:
![image](https://github.com/user-attachments/assets/bbe2fc8c-1291-464b-aa8f-d9c8c4ac0e2a)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
