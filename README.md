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
## Developed By: GIFTSON RAJARATHINAM N
## Register Number: 212222233002

```
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('Spb.jpeg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
```
# Load the color image
image = cv2.imread('SPB Dark.jpg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
### Histogram of Grayscale Image:
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

```

### Histogram Equalization of Grayscale Image:
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])




```
## Output:
### Input Grayscale Image 

![Screenshot 2024-10-01 112639](https://github.com/user-attachments/assets/f98ad049-db20-4420-81f6-3ee8c5bd2be2)


### Histogram of Grayscale Image and any channel of Color Image


![Screenshot 2024-10-01 112657](https://github.com/user-attachments/assets/9fc60195-f8a7-4818-899c-3473fa7da544)


### Histogram Equalization of Grayscale Image.


![Screenshot 2024-10-01 112917](https://github.com/user-attachments/assets/114d3f73-bc3b-4770-a298-3ccafac2a622)


![Screenshot 2024-10-01 112927](https://github.com/user-attachments/assets/9b379ee9-7394-4c27-a317-ee4656efe0e8)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
