# EXP.NO-3 : Histogram Equalization Using OpenCV (Grayscale & Color Images)
# Aim
To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

# The program performs the following operations:
 Read and display a grayscale image

 Plot histogram of the grayscale image

 Apply histogram equalization on grayscale image
 
 Read and display a color image

 Plot histogram of B, G, R channels

 Convert image to HSV color space

 Apply histogram equalization on the Value (V) channel

 Convert the enhanced image back to BGR format

 Display original and enhanced images with histograms

# Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib

# Algorithm
Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2:
Read the image parrot.jpg in grayscale format.

Step 3:
Display the grayscale image and plot its histogram.

Step 4:
Apply histogram equalization using cv2.equalizeHist() to enhance contrast.

Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

Step 6:
Read the same image in color format.

Step 7:
Split the image into B, G, R channels and plot their histograms.

Step 8:
Convert the image from BGR to HSV color space.

Step 9:
Apply histogram equalization on the V (Value) channel.

Step 10:
Merge the channels and convert the image back to BGR format.

Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid.

# Program
# Developed By:
# Name: MONISHA S
# Register No:212225040258

# CODE:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

img = cv2.imread('PHOTO.jpeg', cv2.IMREAD_GRAYSCALE)

plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.show()

plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Original Image')
plt.show()

img_eq = cv2.equalizeHist(img)

plt.hist(img_eq.ravel(), 256, range = [0, 256])
plt.title('Equalized Histogram')

plt.imshow(img_eq, cmap='gray')
plt.title('Original Image')
plt.show()

img = cv2.imread('PHOTO.jpeg', cv2.IMREAD_COLOR)

img_hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)

img_hsv[:,:,2] = cv2.equalizeHist(img_hsv[:, :, 2])

img_eq = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)

plt.imshow(img_eq[:,:,::-1]); plt.title('Equalized Image');plt.show()

plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized');plt.show()

plt.figure(figsize = (20,10))
plt.subplot(221); plt.imshow(img[:, :, ::-1]); plt.title('Original Color Image')
plt.subplot(222); plt.imshow(img_eq[:, :, ::-1]); plt.title('Equalized Image')
plt.show()

plt.figure(figsize = [15,4])
plt.subplot(121); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(122); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized')
```


# OutputHistogram of an Images
<img width="432" height="557" alt="image" src="https://github.com/user-attachments/assets/0e8a2b35-ec39-45bb-b484-594e0c9d1196" />  
<img width="702" height="547" alt="image" src="https://github.com/user-attachments/assets/ad591e7e-886c-4e28-ae58-69836de6f5be" />
<img width="708" height="543" alt="image" src="https://github.com/user-attachments/assets/75199721-fb8e-400b-9f6a-b1fa07bb489e" />
<img width="441" height="550" alt="image" src="https://github.com/user-attachments/assets/7f6451ca-f20b-4f5a-9ef2-812ddbc04745" />
<img width="723" height="542" alt="image" src="https://github.com/user-attachments/assets/397701a8-3764-4e00-9fa0-d2982980517d" />

<img width="1377" height="478" alt="image" src="https://github.com/user-attachments/assets/ba1badaa-0ded-489a-999d-6c435a758bc6" />

<img width="1387" height="428" alt="image" src="https://github.com/user-attachments/assets/95848167-c099-4c42-861a-50f1d1164031" />

# RESULT:
Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.








