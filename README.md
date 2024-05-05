## OPENING--AND-CLOSING
### Aim
To implement Opening and Closing using Python and OpenCV.

### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:
Import the necessary packages
#### Step2:
Create the Text using cv2.putText
#### Step3:
Create the structuring element
#### Step4:
Use Opening operation
#### Step5:
Use Closing Operation

### Program:
```
Developed by: MAHESH RAJ PUROHIT J
Register Number:212222240058
```
#### Display the input Image
```
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'MAHESH', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
#### Create ths structured element
```
struct_ele = np.ones((9, 9), np.uint8)
```
#### Display the result of Opening
```
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
#### Display the result of Closing
```
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
### Output:

#### Display the input Image
![Screenshot 2024-05-05 170536](https://github.com/maheshrajpurohit18/OPENING--AND-CLOSING/assets/118749665/a6dbb678-1862-44ae-ae4f-39ed9fb74e08)


#### Display the result of Opening


![Screenshot 2024-05-05 170644](https://github.com/maheshrajpurohit18/OPENING--AND-CLOSING/assets/118749665/10559198-9c13-42b3-bc03-27e7f39a1fb1)


#### Display the result of Closing

![Screenshot 2024-05-05 170733](https://github.com/maheshrajpurohit18/OPENING--AND-CLOSING/assets/118749665/7cca669f-5b94-4082-ae4a-2d012b36035a)





### Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
