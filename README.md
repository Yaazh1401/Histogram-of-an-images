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
# Developed By: yaazhini S
# Register Number: 212224230308
import cv2
from matplotlib import pyplot as plt
#Load the color image
image = cv2.imread("C:\\Users\\admin\\OneDrive\\Desktop\\DIPT\\flower.jpg")
#Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])

# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')

hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])


```
## Output:
### Input Grayscale Image and Color Image
<img width="793" height="527" alt="image" src="https://github.com/user-attachments/assets/1f21ef10-b481-468f-ac4b-9780a77b66c0" />

### Histogram of Grayscale Image and any channel of Color Image
<img width="870" height="624" alt="image" src="https://github.com/user-attachments/assets/b3f60465-7dcd-44e3-b6b6-6a09a038cd44" />

### Equalization of the image
<img width="816" height="540" alt="image" src="https://github.com/user-attachments/assets/c1a40132-2113-460b-bf7a-4c83b6e4b317" />


### Histogram Equalization of Grayscale Image.
<img width="959" height="606" alt="image" src="https://github.com/user-attachments/assets/554e4ec1-b8a3-4b12-9d97-20518bda1525" />




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
