# EXP-3
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

### Developed By: ASHWIN KUAMR S
### Register Number: 212222240013

```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('dog.png')
color_image = cv2.imread('bird.png',-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```
import numpy as np
import cv2
Gray_image = cv2.imread("dog.png")
Color_image = cv2.imread("bird.png")
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
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```
import cv2
gray_image = cv2.imread("dog.png",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![1](https://github.com/user-attachments/assets/b977164c-3c3e-46b5-8da8-b50f9b0ecfc8)
![2](https://github.com/user-attachments/assets/ae38d318-18fc-4605-a55c-2532ecddf36f)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/user-attachments/assets/1d96be4b-3dcd-4a95-87aa-31891db86cca)
![image](https://github.com/user-attachments/assets/bbf432e2-77c4-430c-8b49-eaef589d5e56)



### Histogram Equalization of Grayscale Image.
![3](https://github.com/user-attachments/assets/7256e4df-a75e-475d-9a8c-e438163dd10a)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
