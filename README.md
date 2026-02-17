# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:q
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

### Program :
```

import cv2
import matplotlib.pyplot as plt

# 1. Read the image using imread
# Replace 'your_image.jpg' with your actual file path
img = cv2.imread('rose.png')

# 2. Convert the color (Note: OpenCV reads in BGR, so we convert BGR to RGB for Matplotlib)
gray = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
gray_single_channel = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) # Often used for processing
gray = cv2.GaussianBlur(gray, (3,3), 0)

# --- Sobel X ---
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
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

# --- Sobel Y ---
# 3. Complete the Sobel Y code
sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5) 
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

# --- Sobel XY ---
sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
# 4. Add the subplot command for the second image
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

# --- Laplacian ---
lap = cv2.Laplacian(gray, cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
# 5. Display the image using imshow
plt.imshow(lap) 
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

# --- Canny ---
canny = cv2.Canny(img, 120, 150) # Canny usually works best on the original or grayscale
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny, cmap='gray')
# 6. Provide the title
plt.title("Canny Edge Detection") 
plt.axis("off")
plt.show()

```

## Output:
### SOBEL EDGE DETECTOR
</br>
</br>
<img width="705" height="287" alt="image" src="https://github.com/user-attachments/assets/b0029ed8-d062-4231-bd45-731f00549e22" />


<img width="712" height="288" alt="image" src="https://github.com/user-attachments/assets/57307b52-2e34-4242-a09a-3e56fd9f181e" />


<img width="708" height="282" alt="image" src="https://github.com/user-attachments/assets/ae0d7bcd-88f7-4136-91ce-f6cb5e967d31" />


</br>
</br>

### LAPLACIAN EDGE DETECTOR
</br>
</br>
<img width="727" height="292" alt="image" src="https://github.com/user-attachments/assets/75e4d7c1-de43-4201-bfc5-732b9796096a" />


</br>
</br>


### CANNY EDGE DETECTOR
</br>
</br>
<img width="703" height="303" alt="image" src="https://github.com/user-attachments/assets/d826b26d-e327-4642-a0fe-fdc89f4cbab9" />

</br>
</br>
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
