
installation
```python
pip install opencv-python
```


import 
```
import cv2
```


load image
```python
img = cv2.imread('image_filepath', <options>)


options:
	-1 - color (for jpg)
	0 - gray scale
	1 - unchanged (for png)
```


resize image by pixel
```python
img = cv2.imread('image_filepath', (0|1|2))
img = cv2.resize(img, (400, 400))
```


resize image by ratio
```python
img = cv2.imread('image_filepath', (0|1|2))
img = cv.resize(img, (0, 0), fx=2, fy=2)  # resize the image the (0, 0) - the first zero is (the width and the second zero is the height) by pixel. 

```


showing the image
```python
img = cv2.imread('image_filepath', (0|1|2))

cv.imshow('image', img)  # show the image
cv.waitKey(0)  # wait infinite amount of time to close the window
cv.destroyAllWindows()  # if key press then it will close all the windows

```


rotate the image
```python
img = cv2.imread('image_filepath', (0|1|2))

# different ways to rotate an image
img = cv.rotate(img, cv.ROTATE_90_COUNTERCLOCKWISE)
img = cv.rotate(img, cv.ROTATE_90_CLOCKWISE)
img = cv.rotate(img, cv.ROTATE_180)

cv.imshow('image', img)
cv.waitKey(0)
cv.destroyAllWindows()
```


random
```python
import cv2
import numpy as np
import cv2 as cv



cap = cv.VideoCapture('hcr2.mp4')
count = 0
while True:
    ret, frame = cap.read()
    count += 1

    #height, width, _ = frame.shape

    frame = cv.resize(frame, (0, 0), fx=0.6, fy=0.6)

    # width = int(frame.get(3))
    # height = int(frame.get(4))

    height, width, _ = frame.shape

    img = cv.line(frame, (0, 0), (width, height), (255,0,0), 5)
    img = cv.line(img, (0, height), (width, 0), (0,255,0), 5)
    img = cv.rectangle(img, (300, 300), (500,500), (128, 128, 128), 5)

    # width = int(cap.get(3))
    # height = int(cap.get(4))
    #cap = cv.resize(frame, (0, 0), fx=0.5, fy=0.5)


    cv.imshow('frame', img)
    if cv.waitKey(1) == ord('q'):
        break
cap.release()
cv.destroyAllWindows()
```






















