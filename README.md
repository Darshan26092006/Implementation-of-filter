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
<img width="717" height="517" alt="download" src="https://github.com/user-attachments/assets/bdfc863a-3086-45e9-a563-2cebcb0bfd6e" />


</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br>
<img width="531" height="380" alt="download" src="https://github.com/user-attachments/assets/68cffe06-57a9-4308-abfa-a0df8f544cbd" />



</br>
</br>

iii)Using Gaussian Filter
</br>
</br>
<img width="515" height="380" alt="download" src="https://github.com/user-attachments/assets/6193b05c-1a06-43cd-83e6-8fdc63f27f38" />



</br>
</br>

iv) Using Median Filter
</br>
</br>
<img width="717" height="517" alt="download" src="https://github.com/user-attachments/assets/d8d1c9dd-ba64-4833-8ea5-187bb07b66ec" />

</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
<img width="515" height="380" alt="download" src="https://github.com/user-attachments/assets/60dcbbfb-ac42-4a79-8f2a-413e7862986c" />



</br>
</br>

ii) Using Laplacian Operator
</br>
</br>

<img width="515" height="380" alt="download" src="https://github.com/user-attachments/assets/d33cac1b-412d-4854-a4f7-b6b26b2c5ea2" />

</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
