# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:


Display the histograms with their respective images.
<br>

### Step4:
Equalize the grayscale image.
<br>

### Step5:
Display the grayscale image.
<br>

## Program:
```python
# Developed By: Mohan raj s
# Register Number:212221230065
```
```python
import cv2
import matplotlib.pyplot as plt
```
```python
# Write your code to find the histogram of gray scale image and color image channels.

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cha.jpeg")
color_image = cv2.imread("ch.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
# Display the histogram of gray scale image and any one channel histogram from color image

import numpy as np
import cv2
Gray_image = cv2.imread("cha.jpeg")
Color_image = cv2.imread("ch.jpeg")
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
cv2.destroyAllWindows()
```
```python
# Write the code to perform histogram equalization of the image. 

import cv2
gray_image = cv2.imread("cha.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot from 2023-08-30 13-13-09](https://github.com/chandrumathiyazhagan/HISTOGRAM/assets/119393023/d632afde-c10c-4716-8a4c-975430b90e9a)
![Screenshot from 2023-08-30 13-12-55](https://github.com/chandrumathiyazhagan/HISTOGRAM/assets/119393023/cd7f303c-4203-47cb-a80e-f3aaeffc98b1)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot from 2023-08-30 13-09-09](https://github.com/chandrumathiyazhagan/HISTOGRAM/assets/119393023/73d9a943-dfc8-4a44-b8aa-4c56152a8f60)
![Screenshot from 2023-08-30 13-09-20](https://github.com/chandrumathiyazhagan/HISTOGRAM/assets/119393023/cb841e05-4727-40a1-887d-a0f2953293cf)

### Histogram Equalization of Grayscale Image
![Screenshot from 2023-08-30 13-23-44](https://github.com/chandrumathiyazhagan/HISTOGRAM/assets/119393023/e2d42691-2a64-4652-a36d-787e23000008)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
