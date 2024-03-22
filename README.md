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
# Developed By: Koti Sai Sankar
# Register Number: 212222240111
```
# Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gian.png")
color_image = cv2.imread("simpson.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Histogram of Grayscale image and color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("Gian.png")
Color_image = cv2.imread("Simpson.jpg")
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
# Histogram equalization of Grayscale image
```
import cv2
gray_image = cv2.imread("Simpson.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-22 125017](https://github.com/MunagalaSrinath/Histogram-of-an-images/assets/118678482/c6457e1c-3d33-4719-8e10-d25b56642aac)


![Screenshot 2024-03-22 125026](https://github.com/MunagalaSrinath/Histogram-of-an-images/assets/118678482/4827ab21-88a9-4dba-87e5-5f0abb66bf78)



### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/MunagalaSrinath/Histogram-of-an-images/assets/118678482/c545080e-5f94-4920-8e70-9a64069299da)


![image](https://github.com/MunagalaSrinath/Histogram-of-an-images/assets/118678482/037a1519-6a87-4fb2-aee6-65d7de61042e)



### Histogram Equalization of Grayscale Image.


![image](https://github.com/MunagalaSrinath/Histogram-of-an-images/assets/118678482/aa1d804a-16e2-4930-b75f-f4a55f1cfb51)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
