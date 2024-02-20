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

![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/67b5a2ab-8815-4bdd-b921-86cfca7ebda7)




### ii)Write the image
```
import cv2
image=cv2.imread('dipimage.jpg',0)
cv2.imwrite('Evangelin.jpg',image)
```
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/1bc87311-01e5-483b-87dc-989004a21e28)

### iii)Shape of the Image
```
import cv2
image=cv2.imread('dipimage.jpg',1)
print(image.shape)
```
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/14e44724-7a7b-4a8d-9749-ede5c42a8cb8)


### iv)Access rows and columns
```
import random
import cv2
image=cv2.imread('dipimage.jpg',1)
image=cv2.resize(image,(350,350))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,555),
                    random.randint(0,555),
                    random.randint(0,555)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/6e5a0201-becd-4515-aee5-fc2dbb216284)


### v)Cut and paste portion of image
```
import cv2
image=cv2.imread('dipimage.jpg',1)
image=cv2.resize(image,(350,350))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/b89d988c-1c05-42d7-bf5a-3f12846643dd)



### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('dipimage.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/360424af-187d-4cc4-9da1-bbc37e1c184c)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/279f0ead-56ea-4b22-92f2-ad6a1b1df221)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/adc41550-d5fc-4c97-b7f2-47e57b7f7363)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/484b7847-b238-40d8-9496-0d0c031e3dd2)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/e692ae01-4e83-4813-bdbc-fd82ff1597a8)


### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('dipimage.jpg')
img = cv2.resize(img,(350,350))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/77b8b50e-7507-4086-83b5-c1931dd56536) ![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/51933f88-a725-44c5-a546-d9de7a410fb6) ![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/c5c6d696-759b-4567-bb33-049f61b8da9f)


### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('dipimage.jpg')
img = cv2.resize(img,(350,350))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/0b109a2a-754b-40a0-990e-62f3522e94ac)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/4675f15c-1164-4670-b9fb-fe12aa9e9f9b)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/112fdbda-ebd1-4880-8a27-f1c7456efee4)


### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('dipimage.jpg',1)
img = cv2.resize(img,(370,370))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/0bf78c60-e6ad-4571-b973-68748733a468)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/a7d0751c-f956-43b4-a9dc-a1c7b6248e6b)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/8d950926-7d95-41e3-9770-8c257ae5ec7a)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/8c1b1777-9003-4cf1-a8a4-28dac774c7a8)


### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("dipimage.jpg",1)
img = cv2.resize(img,(370,370))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/43f380f4-6cdb-4877-ab90-35e306e2ce16)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/b25e2a1d-ae6f-4539-ba39-2fc00346ce05)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/c1f0df53-1b4a-43b9-aa9f-a8d7c807e6f6)
![image](https://github.com/Evangelin-Ruth/COLOR_CONVERSIONS_OF-IMAGE/assets/94219798/3195d8c6-27f7-44bb-9bab-56fb208e5558)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







