# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate  the image

 
## Program:
```
DEVELOPED BY: HARINI V
REGISTER NO.: 212222230044
```

###  Import the necessary packages
```py
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```py
img = np.zeros((100,400), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,"PIKACHU",(5,70),font,2,(255,255,255),5,cv2.LINE_AA)
```
###  Create the structuring element
```py
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
plt.imshow(img)
plt.axis('off')
```
### Erode the image
```py
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
### Dilate the image
```py
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image:
![image](https://github.com/harini1006/erosion--dilation/assets/113497405/ad80c1e4-68a8-469b-ae0f-39364d12d130)



### Display the Eroded Image:
![image](https://github.com/harini1006/erosion--dilation/assets/113497405/1ed292b5-d19c-4594-a58a-3dbfd240249a)



### Display the Dilated Image:
![image](https://github.com/harini1006/erosion--dilation/assets/113497405/cf5a2da4-f3b2-4540-b682-c3d0685bc3ee)

### Result:
Thus the generated text image is eroded and dilated using python and OpenCV.
