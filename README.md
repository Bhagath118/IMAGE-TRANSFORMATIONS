# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7


## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4:
Display the modified image output.

### Step5:
End the program.



## Program:
```python
# Developed By: NISHA D
# Register Number: 212223230143
```
# i)Image Translation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
# Load the image
image = cv2.imread('christ.jpg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)  
```
```
# 1. Translation
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]]) 
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))
```
```
# 2. Scaling
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR) 
```
```
# 3. Shearing
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]]) 
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))
```
```
# 4. Reflection (Flip)
reflected_image = cv2.flip(image_rgb, 1)
```
```
# 5. Rotation
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1) 
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))
```
```
# 6. Cropping
cropped_image = image_rgb[50:300, 100:400]  
```
```
# Plot the original and transformed images
plt.figure(figsize=(12, 8))
```
```
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')
```
```
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')
```
```

plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')
```
```

plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')
```
```

plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')
```
```

plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')
```
```
plt.tight_layout()
plt.show()
```
```
# Plot cropped image separately as its aspect ratio may be different
plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()

```
## Output:
```python
# Developed By: A.BHAGATHKRISHNA
# Register Number: 212223230029
```
![image](https://github.com/user-attachments/assets/8662ee95-7094-4057-96d5-77f226e598bd)



![image](https://github.com/user-attachments/assets/edbd7df5-4949-43b6-b5f6-feaef36201d5)

![image](https://github.com/user-attachments/assets/be34e88a-b9f1-448a-8c9b-1d3a6d4b11fb)

![image](https://github.com/user-attachments/assets/c158fb58-5378-4b96-91fb-fa8add4a793f)

![image](https://github.com/user-attachments/assets/f87047b4-95d6-42e3-94e1-96b66edc7977)

![image](https://github.com/user-attachments/assets/2934c9b5-c2c5-45f1-858a-f9f5ba9330ee)
![image](https://github.com/user-attachments/assets/5cde88c1-ce45-4c1a-a0ae-6c465b3918ec)


## Result: 


Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
