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
# Developed By:LATHISH KANNA.M
# Register Number: 212222230073
```
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat1.jpg")
color_image = cv2.imread("cat2.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("cat1.jpg")
Color_image = cv2.imread("cat2.jpg")
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
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```python
import cv2
gray_image = cv2.imread("cat1.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![314153759-f5f47617-f66d-4bb9-8196-c902c45dec85](https://github.com/Afsarjumail/Histogram-of-an-images/assets/118343395/f232badc-2220-4c1a-ae26-673936eb2cc9)
![314153799-9cb96bf3-d2d1-4f89-981b-a9ddbb6421cc](https://github.com/Afsarjumail/Histogram-of-an-images/assets/118343395/c5ee7b0d-814a-4a76-b637-e885dc4a24b9)


### Histogram of Grayscale Image and any channel of Color Image
![314154384-a1ca0606-334a-41ba-8150-87fddc7c03e5](https://github.com/Afsarjumail/Histogram-of-an-images/assets/118343395/c75bd413-dfd6-415c-9623-5c1f78915c6e)
![314154447-0106ad19-635b-4e8b-9d62-11f18c448cd9](https://github.com/Afsarjumail/Histogram-of-an-images/assets/118343395/23e691a6-ceb1-4939-bc02-2d0704f94476)
![314154542-4d005c00-6270-4fd1-9761-0892d4a0ee8b](https://github.com/Afsarjumail/Histogram-of-an-images/assets/118343395/08172338-e4d6-4186-9ea9-175c4d8b03a3)
![314154574-166106e9-a0d3-41bb-8762-a4d9dbc5fe32](https://github.com/Afsarjumail/Histogram-of-an-images/assets/118343395/d7945fb6-f562-4b11-a79b-ae34372a0cfe)


### Histogram Equalization of Grayscale Image.
![314154625-2b5dfa24-201d-4e68-8a65-5071ad021420](https://github.com/Afsarjumail/Histogram-of-an-images/assets/118343395/622a9cd3-1e8a-473e-bf76-b77d6a1471b8)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
