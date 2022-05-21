# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate

### Step5:
Plot the images using plt.imshow
## Program:

``` python
# Import the necessary packages
import cv2
import numpy as np
import  matplotlib.pyplot as plt


# Create the Text using cv2.putText
import cv2
import numpy as np
import  matplotlib.pyplot as plt
img1 = np.zeros((100,320),dtype = 'uint8')
font  = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(img1,'ANITHA.P',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,'gray')
plt.axis('off')


# Create the structuring element

kernel = np.ones((5,5),np.uint8)

# Erode the image

kernel = np.ones((5,5),np.uint8)
image_erode=cv2.erode(img1,kernel)
plt.imshow(image_erode,'gray')
plt.axis('off')


# Dilate the image
kernel = np.ones((7,2),np.uint8)
image_dilate=cv2.dilate(img1,kernel)
plt.imshow(image_dilate,'gray')
plt.axis('off')

```
## Output:

### Display the input Image
![output](./download.png)

### Display the Eroded Image
![output](./erode.png)



### Display the Dilated Image
![output](./dilated.png)
## Result
Thus the generated text image is eroded and dilated using python and OpenCV.