# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

### Step2:
Read the input image using cv2.imread() and store it in a variable for further processing.

### Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

    Translation moves the image along the x or y-axis.
    Scaling resizes the image by scaling factors.
    Shearing distorts the image along one axis.
    Reflection flips the image horizontally or vertically.
    Rotation rotates the image by a given angle.


### Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

### Step5:
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.
## Program:
```python
Developed By: THRIKESWAR P
Register Number: 212222230162

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('tarantino.jpg')
i)Image Translation
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  # Translate by (50, 100) pixels
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))

# Plot the original and transformed images
plt.figure(figsize=(12, 8))

plt.subplot(2, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')

ii) Image Scaling
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)  # Scale by 1.5x


plt.subplot(2, 3, 3)
plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')




iii)Image shearing
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shear with factor 0.5
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))

plt.subplot(2, 3, 4)
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')




iv)Image Reflection
reflected_image = cv2.flip(image_rgb, 1)  # Horizontal reflection (flip along y-axis)

plt.subplot(2, 3, 5)
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')


v)Image Rotation
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1)  # Rotate by 45 degrees
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))

plt.subplot(2, 3, 6)
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')







vi)Image Cropping
cropped_image = image_rgb[50:300, 100:400]  # Crop a portion of the image

plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()



```
## Output:
### i)Image Translation
![image](https://github.com/user-attachments/assets/65b4bca0-dc0f-47f8-8f2b-fbdab727dd92)


### ii) Image Scaling
![image](https://github.com/user-attachments/assets/5b2c5dde-537e-487f-853d-8c330d1ae39a)



### iii)Image shearing
![image](https://github.com/user-attachments/assets/1f73b14d-9f12-4c6d-8fd2-0770dba41a66)



### iv)Image Reflection
![image](https://github.com/user-attachments/assets/99ec233e-c121-460e-a955-9328866ab5bb)




### v)Image Rotation
![image](https://github.com/user-attachments/assets/2526d2f7-87d6-4582-8ae2-529e4317adc3)




### vi)Image Cropping
![image](https://github.com/user-attachments/assets/02fec19e-9bc8-4003-82e6-451f1bfcb43b)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
