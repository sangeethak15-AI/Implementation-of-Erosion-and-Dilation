# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.

### Step 2:
Create the text image using cv2.putText.

### Step 3:
Then create the structuring image for dilation/erosion.

### Step 4:
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step 5:
Plot the images using plt.imshow.

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,440),dtype = 'uint8')
img=cv2.cvtColor(text_image,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(img,"Sangeetha.K",(5,70),font,2,(255, 229, 180),5,cv2.LINE_AA)
cv2.imshow("Original Image",img)
cv2.waitKey(0)
cv2.destroyAllWindows()



# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Erode the image
erodeimg = cv2.erode(img,kernel)
cv2.imshow("Eroded Image",erodeimg)
cv2.waitKey(0)
cv2.destroyAllWindows()




# Dilate the image

dilateimg = cv2.dilate(img,kernel)
cv2.imshow("Dilated Image",dilateimg)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/93992063/235413975-fa731171-6a59-409c-8176-e35da41bfe17.png)

### Display the Eroded Image
![image](https://user-images.githubusercontent.com/93992063/235414028-43b9aa87-8732-49e1-8c8e-6a3d45eb625b.png)

### Display the Dilated Image
![image](https://user-images.githubusercontent.com/93992063/235414072-cf13bb62-78d2-4c3f-8bc9-aa54241a4b9e.png)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
