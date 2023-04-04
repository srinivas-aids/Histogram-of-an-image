# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Read the gray and color image using imread()

### Step2:
<br>
Print the image using imshow().


### Step3:
<br>
Use calcHist() function to mark the image in graph frequency for gray and color image.


### Step4:
<br>
cv2.equalize() is used to transform the gray image to equalized form.

### Step5:
<br>

The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: U.SRINIVAS
# Register Number: 212221230108
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

import cv2
import matplotlib.pyplot as plt

gray = cv2.imread('1.png')
color= cv2.imread('OIP.png')
plt.imshow(gray)
plt.show()
plt.imshow(color)
plt.show()




# Display the histogram of gray scale image and any one channel histogram from color image


gray_hist = cv2.calcHist([gray],[0],None,[256],[0,255])
plt.figure()
plt.title("Histogram GRAY")
plt.xlabel("grayscale value")
plt.ylabel("pixelcount")
plt.stem(gray_hist)
plt.show()

color_hist = cv2.calcHist([color],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram COLOR")
plt.xlabel('color value')
plt.ylabel('pixel count')
plt.stem(color_hist)
plt.show()


# Write the code to perform histogram equalization of the image. 

import cv2
gray=cv2.imread('1.png',0)
equ = cv2.equalizeHist(gray)
cv2.imshow('GRAY IMAGE',gray)
cv2.imshow('EQUALIZED IMAGE',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()





```
## Output:
### Input Grayscale Image and Color Image

<img width="500" alt="image" src="https://user-images.githubusercontent.com/93427183/229840297-999b3078-6456-4d3d-86e0-cb9b166a88ee.png">


### Histogram of Grayscale Image and any channel of Color Image

<img width="441" alt="image" src="https://user-images.githubusercontent.com/93427183/229840693-91cda328-6eda-4457-b05d-77d672faeb9f.png">


### Histogram Equalization of Grayscale Image

<img width="1080" alt="image" src="https://user-images.githubusercontent.com/93427183/229840846-0d3b5b11-34aa-4899-a0f3-24154d45595e.png">


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
