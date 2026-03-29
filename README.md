# EDGE-DETECTION
# NAME : VIRUMAA HARISH M
# REG NO : 212223230246
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
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
Name : VIRUMAA HARISH M
Reg No: 212223230246
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
<img width="799" height="415" alt="image" src="https://github.com/user-attachments/assets/a90debc3-b85e-4c5d-826f-8dfd94b559c7" />


<img width="842" height="417" alt="image" src="https://github.com/user-attachments/assets/7a20e2da-15e8-4769-81c6-2f27b6b07644" />

<img width="810" height="419" alt="image" src="https://github.com/user-attachments/assets/28a0fc5e-32b4-4f4e-9b03-e7fb77495c55" />

</br>
</br>

### LAPLACIAN EDGE DETECTOR
</br>
</br>
<img width="792" height="419" alt="image" src="https://github.com/user-attachments/assets/3823b046-7159-4ea1-9312-c9088a9a496d" />

</br>
</br>


### CANNY EDGE DETECTOR
</br>
</br>
<img width="791" height="412" alt="image" src="https://github.com/user-attachments/assets/70723d46-2662-4d4a-9d4d-bcf059724aae" />

</br>
</br>
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
