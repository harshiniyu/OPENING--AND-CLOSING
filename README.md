# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element
### Step4:
Use Opening operation

### Step5:
Use Closing Operation

 
## Program:
## Name: Harshini Y
## reg no:212223240050
```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Harsh",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Display the input Image
![Screenshot 2025-05-19 222844](https://github.com/user-attachments/assets/b3c5e40c-c3c5-423b-aedc-effd9eb60fe7)


### Display the result of Opening

![Screenshot 2025-05-19 222853](https://github.com/user-attachments/assets/d5840340-71ca-46c5-91a7-f687e232ff34)

### Display the result of Closing
![Screenshot 2025-05-19 222903](https://github.com/user-attachments/assets/81f3f9b1-fe1c-4f54-9ef6-aa648bb29587)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
