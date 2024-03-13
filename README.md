# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
### Colour and Gray Image
```python
# Developed By: Priyanka A
# Register Number: 212222230113


import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grayflower.jpg")
color_image = cv2.imread("colourflower.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Histogram of Grayscale Image

```py

import numpy as np
import cv2
Gray_image = cv2.imread("grayflower.jpg")
Color_image = cv2.imread("colourflower.jpg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()

```
### Histogram of Green channel of colour Image

```py

plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
  ```


### Histogram Equalization of Grayscale Image

```py

import cv2
gray_image = cv2.imread("colourflower.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/PriyankaAnnadurai/Histogram-of-an-images/assets/118351569/949e1e07-2a2e-4e00-a7e2-9d4b94a1a1ce)


### Histogram of Grayscale Image
![image](https://github.com/PriyankaAnnadurai/Histogram-of-an-images/assets/118351569/5a2e15b9-1b06-4c17-9704-f19806aa0c24)

![image](https://github.com/PriyankaAnnadurai/Histogram-of-an-images/assets/118351569/a7110e16-5625-4af9-804f-1baf3de05adb)

### Histogram of Green channel of Color Image

![image](https://github.com/PriyankaAnnadurai/Histogram-of-an-images/assets/118351569/ce218339-d5d2-4870-b01c-03bd3931d8df)

![image](https://github.com/PriyankaAnnadurai/Histogram-of-an-images/assets/118351569/9df69929-a03a-44f8-b7c8-60d094b82f1c)

### Histogram Equalization of Grayscale Image.

![image](https://github.com/PriyankaAnnadurai/Histogram-of-an-images/assets/118351569/7195bb31-ec11-4c09-9a7f-6ef85a057f7f)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
