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
### Developed By:
### Register Number: 


## Output:

### i) Read and display the image

 ```
    import cv2
    image=cv2.imread('dip.jpg',1)
    image=cv2.resize(image,(500,500))
    cv2.imshow('SHALINI V',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    ```
![image](https://github.com/shalini-venkatesan/COLOR_CONVERSIONS_OF-IMAGE/assets/118720291/c6eb0f15-dd8d-4489-b191-f5c4b2b4e938)


### ii)Write the image

 ```
    import cv2
    image=cv2.imread('dip.jpg',0)
    cv2.imwrite('demos.jpg',image)
    ```
 ![image](https://github.com/shalini-venkatesan/COLOR_CONVERSIONS_OF-IMAGE/assets/118720291/3ca499f0-b16d-45fd-9a34-4316282a70ed)


### iii)Shape of the Image

 ```
    import cv2
    image=cv2.imread('dip.jpg',1)
    print(image.shape)
    ```
![image](https://github.com/shalini-venkatesan/COLOR_CONVERSIONS_OF-IMAGE/assets/118720291/56fb0550-e2e5-4d8a-bd71-66595d74967e)


### iv)Access rows and columns
 ```
    import random
    import cv2
    image=cv2.imread('dip.jpg',1)
    image=cv2.resize(image,(500,500))
    for i in range (250,500):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    ```
 ![image](https://github.com/shalini-venkatesan/COLOR_CONVERSIONS_OF-IMAGE/assets/118720291/16758150-006c-4e09-8093-471bbeb70318)


### v)Cut and paste portion of image
<br> ```
   import cv2
   image=cv2.imread('dip.jpg',1)
   image=cv2.resize(image,(500,500))
   tag =image[150:200,110:160]
   image[110:160,150:200] = tag
   cv2.imshow('image1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
   ```
<br> ![image](https://github.com/shalini-venkatesan/COLOR_CONVERSIONS_OF-IMAGE/assets/118720291/98f2dcfc-2da0-41dd-83bc-d7d9d4036246)


### vi) BGR and RGB to HSV and GRAY
<br> ```
import cv2
img = cv2.imread('dip.jpg',1)
img = cv2.resize(img,(200,200))
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

<br> ![image](https://github.com/shalini-venkatesan/COLOR_CONVERSIONS_OF-IMAGE/assets/118720291/14d43a24-326c-4cc9-b403-301e8e0170bf)


### vii) HSV to RGB and BGR
<br> ```
import cv2
img = cv2.imread('dip.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br> ![image](https://github.com/shalini-venkatesan/COLOR_CONVERSIONS_OF-IMAGE/assets/118720291/467b8786-2736-42b5-b666-e334cc68297f)


### viii) RGB and BGR to YCrCb
<br> ```
import cv2
img = cv2.imread('dip.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>

### ix) Split and merge RGB Image
<br>
<br>

### x) Split and merge HSV Image
<br>
<br>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







