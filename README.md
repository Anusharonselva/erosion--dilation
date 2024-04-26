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
Dilate the Image
 
## Program:
```
DEVELOPED BY: S.ANUSHARON
REG.NO: 212222240010
```
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img = np.zeros((100,500),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'S.ANUSHARON',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```


# Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
````
## Output:

### Display the input Image

![Screenshot 2024-04-26 093512](https://github.com/Anusharonselva/erosion--dilation/assets/119405600/8e02373d-5be4-4ff8-80ab-8dbb4526832c)

### Display the Eroded Image
![Screenshot 2024-04-26 093547](https://github.com/Anusharonselva/erosion--dilation/assets/119405600/56466921-da7c-4041-912e-97118fe71a48)


### Display the Dilated Image
![Screenshot 2024-04-26 093557](https://github.com/Anusharonselva/erosion--dilation/assets/119405600/89e8e244-f3cb-4ea2-b62d-1a7f81a84263)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
