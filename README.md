# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.


## Program:
### Developed By   : SANDHIYA P
### Register Number: 212223230183
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("tree.png")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
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
```Python

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
iii) Using Gaussian Filter
```Python



gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()


```
iv)Using Median Filter
```Python


median=cv2.medianBlur(image2,13)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()


```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```Python



kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()



```
ii) Using Laplacian Operator
```Python


laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()


```

## OUTPUT:
### Original Image

![Screenshot 2025-04-24 135221](https://github.com/user-attachments/assets/b78e1795-3e84-4247-b043-2ccb19613475)

### 1. Smoothing Filters

# i) Using Averaging Filter
![Screenshot 2025-04-24 135228](https://github.com/user-attachments/assets/06eb4c94-b8b0-4b3d-8e02-18978c46feea)


# ii)Using Weighted Averaging Filter

![Screenshot 2025-04-24 135234](https://github.com/user-attachments/assets/c6cdf2bc-0405-41c7-9296-5d7e5750facf)

# iii)Using Gaussian Filter
![Screenshot 2025-04-24 135240](https://github.com/user-attachments/assets/864d71f4-975b-4a36-a834-10d8a23fb7da)


# iv) Using Median Filter
![Screenshot 2025-04-24 135246](https://github.com/user-attachments/assets/b11bdfd8-4489-43fd-b4dd-2dd6b2700720)


### 2. Sharpening Filters
</br>

# i) Using Laplacian Kernal

![Screenshot 2025-04-24 135253](https://github.com/user-attachments/assets/2a74c58b-2d50-4cf2-9597-6495d663b8b1)

# ii) Using Laplacian Operator

![Screenshot 2025-04-24 135259](https://github.com/user-attachments/assets/269c5f4d-61c1-4ce9-9a4e-f39634bf9f11)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
