# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>
Import the necessary packages.

### Step2:
<br>
Create the Text using cv2.putText.

### Step3:
<br>
Create the structuring element.

### Step4:
<br>
Erode and Dilate the image.

### Step5:
<br>
End Program.
 
## Program:

``` Python
# Developed By   : DHIVYA SHRI B
# Register Number: 212221230009

# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt


# Create the text using cv2.putText
text_image = np.zeros((100,250),dtype = 'uint8')
font = cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(text_image,"DHIVYA",(5,70),font,2,(255),2,cv2.LINE_AA) 
plt.title("Original Image")
plt.imshow(text_image,'binary')
plt.axis('off')


# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(4,4))


# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'binary')
plt.axis('off')



# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'binary')
plt.axis('off')




```
## Output:

### Display the input Image
<br>
<br>
<br>
<br>
<br>
<br>
<img width="200" alt="A" src="https://github.com/DhivyaShri484/Implementation-of-Erosion-and-Dilation/assets/94505585/558271da-8e38-4664-b88b-fd1663eeb4e9">




### Display the Eroded Image
<br>
<br>
<br>
<br>
<br>
<br>
<img width="187" alt="B" src="https://github.com/DhivyaShri484/Implementation-of-Erosion-and-Dilation/assets/94505585/66d938ee-04b3-465e-8a87-c3b438e82e18">

### Display the Dilated Image
<br>
<br>
<br>
<br>
<br>
<br>
<img width="196" alt="C" src="https://github.com/DhivyaShri484/Implementation-of-Erosion-and-Dilation/assets/94505585/512c3802-0f8b-44f5-8671-d40144548642">


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
