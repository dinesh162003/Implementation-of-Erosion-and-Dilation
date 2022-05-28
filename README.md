# IMPLEMENTATION OF EROSION AND DILATION
## AIM:
To implement Erosion and Dilation using Python and OpenCV.
## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Erode the image.
### Step 5:
Dilate the image.

## PROGRAM:
```
/*
Developed by   : S.Dinesh
Register Number: 212220230011
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(image,'Dinesh',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(image)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Erode the image
image_erode1=cv2.erode(image,kernel)
plt.axis('off')
plt.imshow(image_erode1)
plt.show()

# Dilate the image
image_dilate1=cv2.dilate(image,kernel)
plt.axis('off')
plt.imshow(image_dilate1)
plt.show()
```
## OUTPUT:

### Display the input Image
![image](https://user-images.githubusercontent.com/75235159/170826205-d8839f88-4b61-4324-a933-742c957ba1db.png)

### Display the Eroded Image
![image](https://user-images.githubusercontent.com/75235159/170826226-0ae0d408-21c1-4295-a5cf-ba5df639ce95.png)

### Display the Dilated Image
![image](https://user-images.githubusercontent.com/75235159/170826243-cc98d847-4adc-4db4-ad68-38860331ba1a.png)

## RESULT:
Thus the generated text image is eroded and dilated using python and OpenCV.
