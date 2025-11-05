# Implementation-of-Erosion-and-Dilation
### Reg No:212223240068
### Name : Karuniya M
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale


### Step2:
Define a structuring element (kernel) for morphological operations.

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.

### Step5:
Display and compare the original, eroded, and dilated images.
 
## Program:

```

# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Create the Text using cv2.putText


font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'KARUNIYA M', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Create the structuring element

kernel = np.ones((3, 3), np.uint8)


# Erode the image

eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')


# Dilate the image


dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')


```
## Output:

### Display the input Image

<img width="496" height="501" alt="image" src="https://github.com/user-attachments/assets/c8bdf437-7ab1-42c6-83a6-e0a3bc68a341" />


### Display the Eroded Image

<img width="518" height="493" alt="image" src="https://github.com/user-attachments/assets/58d1c13c-9b73-49f2-85b6-9059a33f5b8a" />


### Display the Dilated Image

<img width="522" height="506" alt="image" src="https://github.com/user-attachments/assets/603962c4-7189-43b9-9650-803b75d5b0e2" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
