# Implementation-of-filter

### Developed By   :  Darshan V
### Register Number: 212224230050

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Using Averaging Filter
</br> 

### Step2
</br>
Using Weighted Averaging Filter
</br> 

### Step3
</br>
Using Gaussian Filter
</br> 

### Step4
</br>
Using Median Filter
</br> 

### Step5
</br>
Using Laplacian Kernal
</br>

### Step6
</br>
Using Laplacian Operator
</br> 

## Program:

</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("rose.png")
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
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
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
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()

```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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
</br>

i) Using Averaging Filter
</br>
</br>
<img width="717" height="517" alt="download" src="https://github.com/user-attachments/assets/d755dc49-8b7e-423f-9e3e-2ace612e2034" />

</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br>
<img width="531" height="380" alt="download" src="https://github.com/user-attachments/assets/328621d0-c75b-455b-8cee-dc6a25d78e41" />


</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
<img width="515" height="380" alt="download" src="https://github.com/user-attachments/assets/705c647d-d9d6-41f9-935a-7226faf50e24" />


</br>
</br>

iv) Using Median Filter
</br>
</br>
<img width="717" height="517" alt="download" src="https://github.com/user-attachments/assets/cc2a46bf-ef9c-47bb-b56c-69f684c6cc1e" />

</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
<img width="515" height="380" alt="download" src="https://github.com/user-attachments/assets/6841e878-e852-44b7-a2d5-140f4e56575d" />


</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
<img width="515" height="380" alt="download" src="https://github.com/user-attachments/assets/758a682f-76a8-49ae-ac39-f54b3e7580cc" />

</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
