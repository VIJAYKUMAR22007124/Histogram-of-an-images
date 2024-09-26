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
# Developed By:  VIJAY KUMARB
# Register Number: 212222230173


!pip install opencv-python

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('TB.jpg')
color_image = cv2.imread('CATC.jpEg')
cv2.imshow("Gray image",gray_image)
cv2.imshow("color image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

import numpy as np
gray_image=cv2.imread('TB.jpg')
import matplotlib.pyplot as plt 
gray_hist=cv2.calcHist(gray_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale value")
plt.ylabel("pixel count")
plt.stem(gray_hist)
plt.show()

import numpy as np
color_image=cv2.imread('CATC.jpg')
import matplotlib.pyplot as plt 
color_hist=cv2.calcHist(color_image,[0],None,[255],[0,255])
plt.figure()
plt.imshow(color_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Colorscale value")
plt.ylabel("pixel count")
plt.stem(color_hist)
plt.show()

import cv2
gray_image = cv2.imread("gray_image.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### Input Grayscale Image and Color Image

![Screenshot 2024-09-26 143614](https://github.com/user-attachments/assets/60731fc8-c53e-4fa4-8c19-ab0e60439d2a)


### Histogram of Grayscale Image and any channel of Color Image

![Screenshot 2024-09-26 143718](https://github.com/user-attachments/assets/5e4018ee-662c-45d0-8dbd-dd5ff60faab2)

![Screenshot 2024-09-26 143729](https://github.com/user-attachments/assets/139c4579-400c-4a48-84ac-35c13679e96c)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/ec0c32f8-2070-4d56-a8ca-b95625e8777f)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
