# OPENING--CLOSING
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

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.
 
## Program:
```
DEVELOPED BY: MAHESH RAJ PUROHIT J
REGISTER NO: 212222240058
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'MAHESH', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
### Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
### Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image
![Screenshot 2024-05-05 165516](https://github.com/maheshrajpurohit18/OPENING--AND-CLOSING/assets/118749665/273c512b-7d0c-4cd4-8c7a-6091f3be6931)



### Display the result of Opening

![Screenshot 2024-05-05 165531](https://github.com/maheshrajpurohit18/OPENING--AND-CLOSING/assets/118749665/f4b370dd-4d22-4637-b64a-c396bcfb9255)


### Display the result of Closing

![Screenshot 2024-05-05 165547](https://github.com/maheshrajpurohit18/OPENING--AND-CLOSING/assets/118749665/09720794-02fe-4ecf-9068-e8ca3e132867)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
