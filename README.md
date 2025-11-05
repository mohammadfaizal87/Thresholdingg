# THRESHOLDING
## Name: MOHAMMAD FAIZAL SK
## Reg no:212223240092

## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results

## Program
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
## Output
### Original Image
<img width="840" height="244" alt="Screenshot 2025-10-08 000818" src="https://github.com/user-attachments/assets/45f4dc42-6e0f-4c0a-ae2f-bf32ea05c8b6" />


### Global Thresholding
<img width="402" height="196" alt="Screenshot 2025-10-08 000858" src="https://github.com/user-attachments/assets/bb81991a-d89c-4ffa-a26e-e5ded6fcc6b1" />


### Adaptive Thresholding
<img width="379" height="208" alt="Screenshot 2025-10-08 000926" src="https://github.com/user-attachments/assets/32ffe9cf-d917-4283-88e0-08832ebc5029" />


### Optimum Global Thesholding using Otsu's Method
<img width="379" height="194" alt="Screenshot 2025-10-08 000953" src="https://github.com/user-attachments/assets/07d82f05-14ae-4a8f-936c-f8e624861c35" />



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
