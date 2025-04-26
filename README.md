# THRESHOLDING
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
Use Otsu's method to segment the image and display the results.

## Program
### Name : Dharshni V M
### Register Number : 212223240029

```
# Load the necessary packages
import numpy as np
import matplotlib.pyplot as plt
import cv2

# Read the Image and convert to grayscale
image = cv2.imread("kakashi.png",1)
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
image_gray = cv2.imread("kakashi.png",0)

# Use Global thresholding to segment the image
ret,thresh_img1=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(image_gray,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(image_gray,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(image_gray,100,255,cv2.THRESH_TRUNC)

# Use Adaptive thresholding to segment the image
thresh_img7=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img8=cv2.adaptiveThreshold(image_gray,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)

# Use Otsu's method to segment the image 
ret,thresh_img6=cv2.threshold(image_gray,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)

# Display the results
plt.axis("off")
plt.title("Original Image")
plt.imshow(image)

plt.axis("off")
plt.title("Gray Image")
plt.imshow(cv2.cvtColor(image_gray, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

plt.axis("off")
plt.title("Threshold Image (Binary)")
plt.imshow(cv2.cvtColor(thresh_img1, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

plt.axis("off")
plt.title("Threshold Image (Binary Inverse)")
plt.imshow(cv2.cvtColor(thresh_img2, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

plt.axis("off")
plt.title("Threshold Image (Binary Inverse)")
plt.imshow(cv2.cvtColor(thresh_img2, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

plt.axis("off")
plt.title("Threshold Image (To Zero-Inverse)")
plt.imshow(cv2.cvtColor(thresh_img4, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

plt.axis("off")
plt.title("Threshold Image (Truncate)")
plt.imshow(cv2.cvtColor(thresh_img5, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

plt.axis("off")
plt.title("Otsu")
plt.imshow(cv2.cvtColor(thresh_img6, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

plt.axis("off")
plt.title("Adaptive Threshold (Mean)")
plt.imshow(cv2.cvtColor(thresh_img7, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

plt.axis("off")
plt.title("Adaptive Threshold (Gaussian)")
plt.imshow(cv2.cvtColor(thresh_img8, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()

```
## Output

### Original Image
![original](https://github.com/user-attachments/assets/c823535d-7d68-463e-9f52-f9a0622e2616)

### GREY IMAGE
![gray](https://github.com/user-attachments/assets/5424644a-5a1e-46c2-a33c-db831ab8f769)

### Threshold Image (Binary)
![thresold](https://github.com/user-attachments/assets/1f24096f-1ea1-4882-bd76-99bc8819407e)

### Threshold Image (Binary Inverse)
![binary thresold](https://github.com/user-attachments/assets/1fd3194a-73b2-469e-85fa-f0f8d645db56)

### Threshold Image (To Zero)
![thresold to zero](https://github.com/user-attachments/assets/33f4db4f-fdda-40d6-b510-78010fc57d51)

### Threshold Image (To Zero-Inverse)
![zero inverse thresold](https://github.com/user-attachments/assets/c8cbc2ca-cb7b-4afb-afcc-d221f2197900)

### Threshold Image (Truncate)
![truncate](https://github.com/user-attachments/assets/cf067227-b596-4567-89a9-4e5d71078e7b)

### Otsu
![otsu](https://github.com/user-attachments/assets/d9403c87-0d00-4279-b711-2b0d4f4ef4de)

### Adaptive Threshold (Mean)
![adaptive mean](https://github.com/user-attachments/assets/79513ee2-75ea-4886-85bc-7eb8347c7d65)

### Adaptive Threshold (Gaussian)
![adaptive gaussian](https://github.com/user-attachments/assets/baf5fdbc-e4e4-4da3-b3e7-467ee34f838f)

## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
