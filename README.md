# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Import required libraries.

### Step2:
Read the image and convert it to grayscale then display it.

### Step3:
Use Global thresholding to segment the image

### Step4:
Use Adaptive thresholding to segment the image

### Step5:
Use Otsu's method to segment the image 

### Step6:
End the program.

## Program
```
## DEVELOPED BY : VARSHINI D
## REG NO : 212223230234



# Load the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read the Image and convert to grayscale
image = cv2.imread('ironman.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Use Global thresholding to segment the image
ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

# Use Adaptive thresholding to segment the image
th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY, 11, 2)

# Use Otsu's method to segment the image 
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)


# Display the results

plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()

plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()

plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()
```

## Output

### Original Image

![image](https://github.com/user-attachments/assets/fca1f661-2ab1-4581-bfdc-1eea046a5983)


### Global Thresholding

![image](https://github.com/user-attachments/assets/8b7f2132-ac11-40a1-88f8-53006f013881)



### Adaptive Thresholding

![image](https://github.com/user-attachments/assets/4d569f72-8558-45e9-ad02-775eeaf982e2)




### Optimum Global Thesholding using Otsu's Method

![image](https://github.com/user-attachments/assets/93a98469-917e-4032-bab9-bc5905711b0d)




## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
