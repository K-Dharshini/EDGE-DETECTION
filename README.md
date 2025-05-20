# EDGE-DETECTION
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

## Program:
### Developed by: DHARSHINI K
### Register no: 212223230047

#### (i) Display the original image
```python
import cv2
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread("frog.jpg")  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Display Original Image
plt.imshow(cv2.cvtColor(gray_image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
plt.show()
```

#### (ii) Apply Sobel Edge Detection
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
# Display Sobel Edge Detection
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
```

#### (iii) Apply Laplacian Edge Detection
```python
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
# Display Laplacian Edge Detection
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.show()
```

#### (iv) Apply Canny Edge Detection
```python
canny_edges = cv2.Canny(gray_image, 50, 150)
# Display Canny Edge Detection
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.show()
```

## Output:

### ORIGINAL IMAGE

![image](https://github.com/user-attachments/assets/128d19ce-c56b-4699-bebb-e71bb2d3808f)

### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/f9967f46-1c34-4aee-961b-3fe10d780966)

### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/9f0ee2a0-0690-4f2e-ad12-af5cb61385fe)

### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/b4a194af-4983-464b-a257-8a662cc27419)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
