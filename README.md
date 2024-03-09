# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Install the open cv by using pip install opencv-python
### Step2
Import cv2 for reading and changing it smooth and sharpen image
### Step3
import numpy for give the width and size of a image
### Step4
import matplotlib.pyplot for display the image.
## Program:
### Developed By   : Arikatla hari veera prasad
### Register Number:212223240014
### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('username.jpg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('FILTERED')
plt.axis('off')
```
ii) Using Weighted Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('username.jpg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
kernal2=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('FILTERED')
plt.axis('off')
```
iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('username.jpg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.GaussianBlur(src=image2,ksize=(11,11),sigmaX=0,sigmaY=0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title(' Gaussian Filter')
plt.axis('off')




```

iv) Using Median Filter
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('username.jpg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.medianBlur(src=image2,ksize=11)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Median Blur')
plt.axis('off')



```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('username.jpg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
kernal2=np.array([[0,1,0],[1,-4,1],[0,1,0]])
image3=cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Sharpening Filters')
plt.axis('off')



```
ii) Using Laplacian Operator
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('username.jpg')
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.Laplacian(image2,cv2.CV_64F)
laplacian_image = np.uint8(np.absolute(image3))
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('ORIGINAL')
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(laplacian_image)
plt.title('Sharpening Filters')
plt.axis('off')




```

## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-filter/assets/145049988/15e2adfa-eb17-40db-aeac-9e92d1371361)
ii) Using Weighted Averaging Filter
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-filter/assets/145049988/9e58589d-7787-4b99-8569-66a4b04924ad)
iii) Using Gaussian Filter
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-filter/assets/145049988/539f676b-4439-47fe-84f8-afeab850786a)
iv) Using Median Filter
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-filter/assets/145049988/2d09789c-101d-4a85-aed2-424cd1b47ea6)
### 2. Sharpening Filters
i) Using Laplacian Kernal
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-filter/assets/145049988/f541d0c6-4a04-402a-842f-7fe07793ced2)
ii) Using Laplacian Operator
![image](https://github.com/Hariveeraprasad-2006/Implementation-of-filter/assets/145049988/f11c8d81-0be5-44da-ae9b-22174c62c218)
## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
