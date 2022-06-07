# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the Text using cv2.putText.
<br>

### Step3:
Create the structuring element.
<br>

### Step4:
Use Opening operation.
<br>

### Step5:
Use Closing Operation.
<br>

 
## Program:

``` Python
# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
img1=cv2.putText(img,'CRAZY_THIRU',(5,50),font,1.4,(255),5,cv2.LINE_AA)
plt.imshow(img1)


# Create the structuring element

Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

image1=cv2.morphologyEx(img,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)


# Use Closing Operation

image1=cv2.morphologyEx(img,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)



```
## Output:

### Display the input Image
![1](https://user-images.githubusercontent.com/94980741/172299910-85afb817-be3d-42bd-9b75-884dfab0aea6.jpg)


### Display the result of Opening
![2](https://user-images.githubusercontent.com/94980741/172299914-ae3cb4aa-48e9-47fb-8edc-88f83ef520a7.jpg)


### Display the result of Closing

![3](https://user-images.githubusercontent.com/94980741/172299945-5a19a19d-8bcd-4989-90c9-5103f1afeade.jpg)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
