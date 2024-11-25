



```python

import pyautogui as auto
import cv2 as cv
import numpy as np



# screenshot the
def screenshot(xAxis, yAxis, width, height):
    screenshot = auto.screenshot()
    frame = np.array(screenshot)
    frame = cv.cvtColor(frame, cv.COLOR_RGB2BGR)
    frame = cv.rectangle(frame, (xAxis, yAxis), (width,height), (255, 0, 0), 1)
    return frame

def getMapRegion(frame, xAxis, yAxis, width, height ):
    mapRegion = frame[xAxis : (xAxis+width), yAxis : (yAxis + height)]
    return mapRegion






# PROGRAM START


xAxis = 0
yAxis = 0
width = 338
height = 338


frame = screenshot(xAxis, yAxis, width, height)
mapRegion = getMapRegion(frame, xAxis, yAxis, width, height)

hsvMapRegion = cv.cvtColor(mapRegion, cv.COLOR_BGR2HSV)

#cv.imshow('frame', frame)
cv.imshow('frame', hsvMapRegion)






#cv.imwrite('mapRegion.png', mapRegion)


cv.waitKey(0)
cv.destroyAllWindows()





```

