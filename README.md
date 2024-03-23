# EX-3 Histogram of an images
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


#### Program:
```
### Developed By: Santhosh U
### Register Number: 212222240092
```
<table>
  <tr>
    <td width=50%>
      
####  Histogram of Gray scale image and Color image  
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("grayscale.jpeg")
color_image = cv2.imread("colorscale.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
<td>
  
#### Output:
### Input Grayscale Image and Color Image
![Output1 1](https://github.com/SanthoshUthiraKumar/Histogram-of-an-images/assets/119477975/e10b0d71-1a44-476b-b47e-02d5028e1614)
![Output1 2](https://github.com/SanthoshUthiraKumar/Histogram-of-an-images/assets/119477975/1fe1a782-00dd-46b4-a5fc-2f4295ec15b7)

</td>
</tr>



<tr>
  <td width=50%>

### Histogram of Grayscale image and any color image
```python
import numpy as np
import cv2
Gray_image = cv2.imread("grayscale.jpeg")
Color_image = cv2.imread("colorscale.jpeg")
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
</td>
<td>

### Output:
#### Histogram of Grayscale image and any color image
### Grayscale image
![Output2](https://github.com/SanthoshUthiraKumar/Histogram-of-an-images/assets/119477975/ac82014b-d3de-475f-98b3-0f4a9eff3a48)

### Color image
![Output3](https://github.com/SanthoshUthiraKumar/Histogram-of-an-images/assets/119477975/b31e01d3-0748-45f6-9e20-69f61bf67588)

</td>
</tr>



<tr>
  <td width=50%>

### Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("grayscale.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
<td>
  
### Output:
### Histogram Equalization of Grayscale Image.
![Output3,1](https://github.com/SanthoshUthiraKumar/Histogram-of-an-images/assets/119477975/add86b56-158d-488c-a7ac-197ec0f4da33)
![Output3 2](https://github.com/SanthoshUthiraKumar/Histogram-of-an-images/assets/119477975/49348797-0a8c-44f6-b359-f440209a9267)

</td>
</tr>
</table>

### Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
