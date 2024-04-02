# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.
<br>
### Step2:
Read the image and convert the bgr image to gray scale image.
<br>
### Step3:
Use any filters for smoothing the image to reduse the noise.
<br>
### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.
<br>
### Step5:
Display the filtered image using plot and imshow.
<br>

## Program:

```
DEVELOPED BY: SATHISH R
REG NO : 212222230138
```
# Import the packages
```
import cv2
import matplotlib.pyplot as pl
```
# Load the image, Convert to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dipt_7_img.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR
## SOBEL X
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
## SOBEL Y
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
## SOBEL XY
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```

# CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
#### SOBEL X

![dip_exp_7_1](https://github.com/r-sathish-02/EDGE-DETECTION/assets/118787261/ee626067-ce06-4518-b815-eb8d33008a23)


#### SOBEL Y
![dipt_exp_6_2](https://github.com/r-sathish-02/EDGE-DETECTION/assets/118787261/bfa9c3d0-0ffe-429d-a918-d0dcd340b74a)


#### SOBEL XY
![dip_exp_6_3](https://github.com/r-sathish-02/EDGE-DETECTION/assets/118787261/45eb7b77-9a94-4a1a-bfe5-3cf3b70d6afd)


### LAPLACIAN EDGE DETECTOR
![dip_exp_6_4](https://github.com/r-sathish-02/EDGE-DETECTION/assets/118787261/362a3747-4a3e-4fdb-8787-e40d21b0b7a0)


### CANNY EDGE DETECTOR
![dip_exp_6_5](https://github.com/r-sathish-02/EDGE-DETECTION/assets/118787261/50e06422-3c1e-4cc6-a640-6e68c3b6c18c)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
