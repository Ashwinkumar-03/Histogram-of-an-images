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
from matplotlib import pyplot as plt

# Load the color image
image = cv2.imread("v3.jpg")

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

# Apply histogram equalization
equalized_image = cv2.imread("v3.jpg")
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

# Load the GRAY image
image = cv2.imread('v4.jpg')
plt.imshow(image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

# Apply histogram equalization to gray image
equalized_image = cv2.imread('v4.jpg')
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```

## Output:
### Input Grayscale Image and Color Image

![image](https://github.com/user-attachments/assets/3744aa14-223f-4308-818f-b33bf63a9a2e)
![image](https://github.com/user-attachments/assets/301e42bb-5757-4f5d-aeb3-acd45e5acb13)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/user-attachments/assets/41137140-3e5d-4df6-8dab-4c86ebbbff60)
![image](https://github.com/user-attachments/assets/d93b3181-d229-4ae3-a210-304847de9d32)


### Histogram Equalization of Grayscale Image.
![image](https://github.com/user-attachments/assets/9550c521-e495-4ac4-a13c-0694b065795c)
![image](https://github.com/user-attachments/assets/39ba12bd-f4ff-49d3-af12-f8dd96166da4)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
