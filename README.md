# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** Cholimgapuram Sai Likitha

**Register No:** 212224230046
### Original image 
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("img.png")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```
### Original Grayscale Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("img.png", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
### Global Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("img.png", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
### Adaptive Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("img.png", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```
### Otsu's Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("img.png", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```
## Output
### Original image 
<img width="384" height="342" alt="image" src="https://github.com/user-attachments/assets/be921c2f-a825-41b7-a8ed-81f265a635d1" />

### Original Grayscale Image

- The grayscale version of the input image is displayed.
- Serves as the input for thresholding operations.
<img width="394" height="344" alt="image" src="https://github.com/user-attachments/assets/1a20b1ff-e9f1-44b0-95f9-30a25fff9c3f" />


### Global Thresholding

- Original image is displayed.
- Thresholded image is displayed.
- A fixed threshold value is used for segmentation.
- Pixels are classified as foreground or background.
<img width="395" height="347" alt="image" src="https://github.com/user-attachments/assets/69365fce-b586-48aa-9f75-58179eafd426" />


### Adaptive Thresholding

- Original image is displayed.
- Adaptive Mean Thresholded image is displayed.
- Adaptive Gaussian Thresholded image is displayed.
- Threshold values vary across different regions of the image.
- Suitable for images with uneven illumination.
<img width="374" height="348" alt="image" src="https://github.com/user-attachments/assets/27a98b5a-1c93-4770-99d4-00aeea2d7042" />

### Otsu's Thresholding

- Original image is displayed.
- Otsu segmented image is displayed.
- Optimal threshold value is calculated automatically.
- Produces improved segmentation for bimodal histograms.
<img width="373" height="342" alt="image" src="https://github.com/user-attachments/assets/a16c36c3-caa9-4995-ae23-204cf880c11d" />


## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
