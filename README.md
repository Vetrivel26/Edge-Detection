# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step1:
Import the required packages for further process.

Step2:
Read the image and convert the bgr image to gray scale image.

Step3:
Use any filters for smoothing the image to reduse the noise.

Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

Step5:
Display the filtered image using plot and imshow.

 

## Program:

``` 
Program to perform edge detection using Sobel, Laplacian, and Canny edge detectors.
Developed by:Aavula Tharun.
Ref.no:212221240003.



import cv2
import matplotlib.pyplot as plt
image = cv2.imread("tom.jpg")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)

## SOBEL EDGE DETETCTOR:
### SOBEL X:

sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL Y:

sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()

### SOBEL XY:

sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()


## LAPLACIAN EDGE DETECTOR:

laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()


## CANNY EDGE DETECTOR:

canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()




```
## Output:
### SOBEL EDGE DETECTOR
#### SOBEL X:
![1 2](https://user-images.githubusercontent.com/93427201/168774631-e0a8eb62-2d22-47bb-8e59-b0afdbfb9c6f.png)
#### SOBEL Y:
![ex 07  2](https://user-images.githubusercontent.com/93427201/168775197-d761b82e-5aa3-47a4-bfe9-1a378a57fb93.png)

#### SOBEL XY:
![ex 07 3](https://user-images.githubusercontent.com/93427201/168774840-927a6065-570e-4485-8b48-b7b6ba16d103.png)

### LAPLACIAN EDGE DETECTOR
![ex 07 4](https://user-images.githubusercontent.com/93427201/168774893-eee22dd0-505c-4985-a4c2-64fd2df0cf6a.png)


### CANNY EDGE DETECTOR
![ex 07 5](https://user-images.githubusercontent.com/93427201/168774925-16e89aa7-eed1-4643-b9ae-8ce47c777851.png)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
