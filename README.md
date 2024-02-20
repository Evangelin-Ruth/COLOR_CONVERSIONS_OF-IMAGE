# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:EVANGELIN.S
### Register Number: 212221230025


## Output:
### Image
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/eaa2578f-4317-4ab4-8a68-b1acddc875a1)

### i) Read and display the image
```
import cv2
image=cv2.imread('dipimage.jpg',1)
image=cv2.resize(image,(350,350))
cv2.imshow('Evangelin',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/67b5a2ab-8815-4bdd-b921-86cfca7ebda7)

<br>


### ii)Write the image

<br>
<br>

### iii)Shape of the Image

<br>
<br>

### iv)Access rows and columns
<br>
<br>

### v)Cut and paste portion of image
<br>
<br>

### vi) BGR and RGB to HSV and GRAY
<br>
<br>

### vii) HSV to RGB and BGR
<br>
<br>

### viii) RGB and BGR to YCrCb
<br>
<br>

### ix) Split and merge RGB Image
<br>
<br>

### x) Split and merge HSV Image
<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







