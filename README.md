# THRESHOLDING
# Name: DODLA SUSMITHA
# Reg no:212224110016
# Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

# Software Required
Anaconda - Python 3.7
OpenCV
# Algorithm
# Step1:
Load the necessary packages.

# Step2:
Read the Image and convert to grayscale.

# Step3:
Use Global thresholding to segment the image.

# Step4:
Use Adaptive thresholding to segment the image.

# Step5:
Use Otsu's method to segment the image and display the results

# Program
# Load the necessary packages
```
import cv2
import matplotlib.pyplot as plt
```
# Read the Image and convert to grayscale
```
image=cv2.imread('Nature.jpg')
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
# Original image:
```
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
# Use Global thresholding to segment the image
```
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)
```
# Use Adaptive thresholding to segment the image
```
adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
```
# Use Otsu's method to segment the image
```
_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
```
# Global Thresholding:
```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
# Adaptive Thresholding:
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
# Otsu's Method:
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
# Show the plot:
```
plt.tight_layout()
plt.show()
```
# Output
# Original Image
<img width="1175" height="462" alt="Screenshot 2026-09-11 220537" src="https://github.com/user-attachments/assets/94b00841-df8c-4100-9806-efa972c30575" />

# Global Thresholding
<img width="1093" height="460" alt="Screenshot 2026-09-11 220555" src="https://github.com/user-attachments/assets/714f5f3b-b658-49f2-a7f6-55218cc1f59e" />

# Adaptive Thresholding
<img width="1063" height="472" alt="Screenshot 2026-09-11 220607" src="https://github.com/user-attachments/assets/86a4733b-1eaf-4bdd-9c5a-34dec3eba75c" />

# Optimum Global Thesholding using Otsu's Method
<img width="1078" height="467" alt="Screenshot 2026-09-11 220618" src="https://github.com/user-attachments/assets/f0dff9fd-e01e-423a-8f0c-a454f20ff361" />

# Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
