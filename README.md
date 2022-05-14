# Implementation-of-Filters
## AIM:
To implement filters for smoothing and sharpening the images in the spatial domain.
## SOFTWARE REQUIRED:
Anaconda - Python 3.7
## ALGORITHM:
### Step 1:
Import the necessary modules. 
### Step 2:
For performing smoothing operation on a image. 
- Average filter
```
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
```
- Weighted average filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
```
- Gaussian Blur 
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
```
- Median filter
```
median=cv2.medianBlur(image2,13)
```
### Step 3:
For performing sharpening on a image.
- Laplacian Kernel
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
```
- Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
```
### Step 4:
Display all the images with their respective filters.
## PROGRAM:
# Developed By   : J . RITHANIEPRIYANKA
# Register Number: 212220230039
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("a.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```
### 1. Smoothing Filters
i) Using Averaging Filter
```
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv) Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```
### 2. Sharpening Filters
i) Using Laplacian Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```
## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter

![exp6-a](https://user-images.githubusercontent.com/75235132/168417522-b40e1686-fdf4-4a81-8cfa-57ea97d6ac3e.png)

ii) Using Weighted Averaging Filter

![exp6-b](https://user-images.githubusercontent.com/75235132/168417530-5fd4c716-313d-49f5-90d9-91b8d78ca9cf.png)

iii) Using Gaussian Filter

![exp6-c](https://user-images.githubusercontent.com/75235132/168417535-0d1f70cb-a1f7-4e06-a052-1ae6742c530f.png)

iv) Using Median Filter

![exp6-d](https://user-images.githubusercontent.com/75235132/168417539-11e182cc-a5bf-40d6-b591-360b71def1f5.png)

### 2. Sharpening Filters

i) Using Laplacian Kernal

![exp6-e](https://user-images.githubusercontent.com/75235132/168417542-85771f58-fefe-45d3-b58f-294d08896921.png)

ii) Using Laplacian Operator

![exp6-f](https://user-images.githubusercontent.com/75235132/168417547-76881061-1f0f-4f96-9002-3148a177df30.png)

## RESULT:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
