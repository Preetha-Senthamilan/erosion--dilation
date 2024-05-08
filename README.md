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
Name:Preetha S
Reg no:212222230110
```


### Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'HEALTH',(60,70),font,2,(255),5,cv2.LINE_AA)
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
```
## Output:

### Display the input Image

![image](https://github.com/Preetha-Senthamilan/erosion--dilation/assets/119390282/30e54128-121e-451b-9dc8-d058fd8c146a)



### Display the Eroded Image

![image](https://github.com/Preetha-Senthamilan/erosion--dilation/assets/119390282/fdc6d12b-552b-4883-a472-2b13738f8bab)


### Display the Dilated Image

![image](https://github.com/Preetha-Senthamilan/erosion--dilation/assets/119390282/57268b17-38be-46d6-8bb0-c9390d8f9627)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
