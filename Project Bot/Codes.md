



```python
import pyautogui as auto
import cv2 as cv
import numpy as np


def screenshot():
    screenshot = auto.screenshot()
    frame = np.array(screenshot)
    frame = cv.cvtColor(frame, cv.COLOR_RGB2BGR)
    return frame

frame = screenshot()

cv.imshow('frame title', frame)


cv.waitKey(0)
cv.destroyAllWindows()





```

