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
# Name: ____________________________
# Register No:

# OutputHistogram of an Images
