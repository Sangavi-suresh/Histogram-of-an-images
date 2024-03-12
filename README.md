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
```python
# Developed By: Sangavi Suresh
# Register Number: 212222230130
```
Input Grayscale Image and Color Image

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("f1.jpeg")
color_image = cv2.imread("f2.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

Histogram of Grayscale Image and any channel of Color Image

import numpy as np
import cv2
Gray_image = cv2.imread("f1.jpeg")
Color_image = cv2.imread(f2.jpeg")
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
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)

Histogram Equalization of Grayscale Image.


import cv2
gray_image = cv2.imread("f2.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()




```
## Output:
### Input Grayscale Image and Color Image

![image](https://github.com/Sangavi-suresh/Histogram-of-an-images/assets/118541861/ed2be0d1-cd1a-4f46-9b5d-63d831eb7717)

![image](https://github.com/Sangavi-suresh/Histogram-of-an-images/assets/118541861/8024cb5c-a600-45b2-b03d-3a6f42215752)


### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/Sangavi-suresh/Histogram-of-an-images/assets/118541861/53d64fe5-4afc-4ff4-9d60-d3a9fc080490)

![image](https://github.com/Sangavi-suresh/Histogram-of-an-images/assets/118541861/e3d88407-6b79-43e4-9e39-1403926d24d2)




### Histogram Equalization of Grayscale Image.




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
