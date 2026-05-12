# Image-Handling-and-Pixel-Transformations-Using-Opencv-

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations. 

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** KIRUBA RC
- **Register Number:** 212224230125

### Ex. No. 01
### Read the image using OpenCV
```PYTHON
img = cv2.imread('eagle.jpg', cv2.IMREAD_COLOR)
```
### Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```PYTHON
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
### # Display the image using Matplotlib
```PYTHON
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
### # Load the image
```PYTHON
image = cv2.imread('eagle.jpg')
```
### Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```PYTHON
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```
### Draw a line from top-left to bottom-right
```PYTHON
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
```
```PYTHON
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```
### Load the image
```PYTHON
image = cv2.imread('eagle.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

```
```python
img_rgb.shape
```
```python
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
```
```python
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```
### Load the image
```python
image = cv2.imread('eagle.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
```python
img.shape
```
### Draw a rectangle around the Whole image
```python
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
```
```python
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```
### Load the image
```python
image = cv2.imread('eagle.jpg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
### Add text to the image
```python
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
```
```python
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
### Load the image
```python
image = cv2.imread('eagle.jpg')
```
```python
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
### Original RGB Image
```python
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```
### Convert RGB to HSV
```python
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
```
### HSV Image
```python
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```
### Convert RGB to GRAY
```python
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
```
### Grayscale Image
```python
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```
### Convert RGB to YCrCb
```python
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
```
### YCrCb Image
```python
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```
### Convert HSV back to RGB
```python
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
```
```python
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```
### Modify a block of pixels (300x300) to white, starting from (200, 200)
```python
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499
```
### Convert BGR to RGB for displaying with Matplotlib
```python
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
### Display the modified image
```python
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```
### Load the image
```python
image = cv2.imread('eagle.jpg')
```
```python
image.shape
```
### Resize the image to half its size
```python
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)
```
### Convert BGR to RGB for displaying with Matplotlib
```python
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)

```
```python
resized_image_rgb.shape
```
### Display the resized image
```python
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()

```
### Load the image
```python
image = cv2.imread('eagle.jpg')
```
```python
image.shape
```
### Convert BGR to RGB for displaying with Matplotlib
```python
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
```
### Display the cropped region (ROI)
```python
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
### Load the image
```python
image = cv2.imread('eagle.jpg')
```
### Flip the image horizontally (left-right)
```python
flipped_horizontally = cv2.flip(image, 1)
```
### Convert BGR to RGB for displaying with Matplotlib
```python
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
```
### Horizontal plt.imshow(flipped_horizontally_rgb)
```python
plt.title("Flipped Horizontally")
plt.axis("off")
flip
```
### Flip the image vertically (up-down)
```python
flipped_vertically = cv2.flip(image, 0)
```
### Convert BGR to RGB for displaying with Matplotlib
```python
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
```
### Vertical flip
```python
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

## Output:
### Read and Display an Image.
<img width="1360" height="525" alt="image" src="https://github.com/user-attachments/assets/ed8ed9bb-53d3-4195-bbaa-2b7a38b3496c" />

### Draw a line from top-left to bottom-right
<img width="1379" height="536" alt="image" src="https://github.com/user-attachments/assets/a179b6a1-7fac-45c5-8a25-9a1b5867f0ce" />

### Image with circle

<img width="1368" height="536" alt="image" src="https://github.com/user-attachments/assets/2a4b3953-246a-4948-a6dd-6a79a4a8b0b1" />

### Image with rectangle
<img width="1387" height="535" alt="image" src="https://github.com/user-attachments/assets/54a5c00e-9b41-480d-9945-7378bed245de" />

### Image with text

<img width="1384" height="532" alt="image" src="https://github.com/user-attachments/assets/75b25f38-cbc1-4fe4-b68d-b17db86fe519" />

### Original RGB Image
<img width="1386" height="532" alt="image" src="https://github.com/user-attachments/assets/45e2238d-fa69-492f-946d-48a8bf5911fc" />

### RGB to HSV

<img width="1383" height="536" alt="image" src="https://github.com/user-attachments/assets/c53349da-55fc-4a45-944d-da8c4e3dfedc" />

### Grayscale Image
<img width="1379" height="526" alt="image" src="https://github.com/user-attachments/assets/97a78c31-ecf2-4328-ba0a-57a831a020f6" />

### YCrCb Image
<img width="1379" height="517" alt="image" src="https://github.com/user-attachments/assets/8727ba52-55f9-4b5b-ba9a-7bd2759ed3a6" />

### HSV back to RGB
<img width="493" height="411" alt="download" src="https://github.com/user-attachments/assets/5a828b06-8cac-458a-a544-5aba0d2f5f7d" />

### Cropped region (ROI)
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/ceb69e8d-6240-41f3-b3f5-1a423edb08c3" />


### block of pixels (300x300) to white, starting from (200, 200)
<img width="493" height="411" alt="download" src="https://github.com/user-attachments/assets/d390754e-ef64-44c5-a710-b384ae754bf5" />

### Horizontal flip
<img width="493" height="411" alt="download" src="https://github.com/user-attachments/assets/03f56c78-e38a-4be2-b5d5-c381a9015d94" />

### Vertical flip
<img width="493" height="411" alt="download" src="https://github.com/user-attachments/assets/e901c9ce-6f5b-4e30-992c-8104f5dfaf02" />



## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.

