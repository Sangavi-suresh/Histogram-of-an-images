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
python
# Developed By: Sangavi Suresh
# Register Number: 212222230130

## Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("f1.jpeg")
color_image = cv2.imread("f2.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Histogram of Grayscale Image and any channel of Color Image
```
import numpy as np
import cv2
Gray_image = cv2.imread("immg.jpeg")
Color_image = cv2.imread("img.jpeg")
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
```
## Histogram Equalization of Grayscale Image.
```

import cv2
gray_image = cv2.imread("immg.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()


```


## Output:
### Input Grayscale Image and Color Image

![314395616-bc1fb72d-4ec4-40a8-b6f7-d2a6ef24fde2](https://github.com/Sangavi-suresh/Histogram-of-an-images/assets/118541861/3f0651c7-ab50-443f-b9d5-0ecda20d4c53)


### Histogram of Grayscale Image and any channel of Color Image

![314395665-b989675c-ca76-4d73-a7b9-6839fefceba8](https://github.com/Sangavi-suresh/Histogram-of-an-images/assets/118541861/0e56da6d-ac1b-4408-a845-6659f8f01522)


![314395699-31fcdd08-6fee-470a-9f75-febf40e05902](https://github.com/Sangavi-suresh/Histogram-of-an-images/assets/118541861/b0382b0c-589a-4ab9-a31c-ba6d15c6cbdf)





### Histogram Equalization of Grayscale Image.

![314395744-ccf046bb-48f1-48f8-9520-e7bb0eddbd6b](https://github.com/Sangavi-suresh/Histogram-of-an-images/assets/118541861/6e304b58-1258-416d-b075-486d509999f4)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
