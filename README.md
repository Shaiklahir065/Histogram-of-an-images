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
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Get the input grayscale image
gray_image = cv2.imread('dog picture.jpg', cv2.IMREAD_GRAYSCALE)

# Step 2: Display the grayscale image
plt.title("Grayscale Image")
plt.imshow(gray_image, cmap='gray')
plt.axis('off')

# Step 3: Plot the histogram of the grayscale image
plt.title("Histogram of Grayscale Image")
plt.hist(gray_image.ravel(), bins=256, color='black', alpha=0.6)
plt.xlim(0, 600)
plt.tight_layout()
plt.show()

# Step 4: Apply histogram equalization using OpenCV
equalized_gray_image = cv2.equalizeHist(gray_image)

# Step 5: Display the histogram of the equalized image
plt.title("Histogram of Equalized Grayscale Image")
plt.hist(equalized_gray_image.ravel(), bins=256, color='black', alpha=0.6)
plt.xlim(0, 600)

# Step 6: Display the enhanced grayscale image
plt.title("Enhanced Grayscale Image")
plt.imshow(equalized_gray_image, cmap='gray')
plt.axis('off')

# Developed By: shaik lahir
# Register Number: 212224240148

```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/user-attachments/assets/f55f3f6b-9c3a-49aa-a26c-ff8be7d9ef44)

![image](https://github.com/user-attachments/assets/5ff76126-6624-4167-a486-a20e7dfd35ae)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/user-attachments/assets/7d572e2f-09df-47c5-bc1e-21247072b926)



### Histogram Equalization of Grayscale Image.

![image](https://github.com/user-attachments/assets/cc907d6f-41ff-4685-ae6c-a236fceedabe)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
