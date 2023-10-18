# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).
<br>
### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.
<br>

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.
<br>

### Step4:
Display the eroded image using cv2.imshow.
<br>

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.
<br>

## Program:
```
Developed by:Dharmaraj S
Register Number:212222240025
```
### Import the necessary packages
``` Python
import cv2
import numpy as np
```
### Create the Text using cv2.putText
```python

img1 = np.zeros((100, 400), dtype="uint8")
font = cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1, "DHARMARAJ S", (5, 70), font, 2, 255, 5, cv2.LINE_AA)
cv2.imshow("Dharmaraj output", img1)
cv2.waitKey(0)

```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


### Erode the image
```python
cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
cv2.imshow("Erode image",image_erode)
cv2.waitKey(0)
```
### Dilate the image
```python
image_dilatel=cv2.dilate(img1,kernel1)
cv2.imshow("Dilate image",image_dilatel)
cv2.waitKey(0)
```
## Output:

### Display the input Image

![1](https://github.com/dharmaraj-007/EROSION-AND-DILATION/assets/119560386/59595276-7720-4fce-b96c-037bc6984f35)


### Display the Eroded Image

![2](https://github.com/dharmaraj-007/EROSION-AND-DILATION/assets/119560386/32efbd6b-1bb1-45f8-8c8e-71405dc78bd6)


### Display the Dilated Image

![3](https://github.com/dharmaraj-007/EROSION-AND-DILATION/assets/119560386/be400482-79ad-4c59-bf71-b7ca7f5293b3)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
