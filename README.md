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

## Program:
```
 Developed By: Nathin R
 Register Number:212222230090 
```

## Image:
![demo](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/b77fd1f2-987c-4711-83c5-cca670a2aac7)

### i) Read and display the image
```
import cv2
image=cv2.imread('demo.jpg',1)
image=cv2.resize(image,(200,325))
cv2.imshow('Nathin',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/39d0370b-f2bc-4077-a100-6cf157630d28)


### ii)Write the image
```
image=cv2.imread('demo.jpg',0)
cv2.imwrite('Nathin.jpg',image)
```
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/1f193c4a-1b7e-41ee-a226-28f44188ca02)

### iii)Shape of the Image
```
print(image.shape)
```
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/8523b467-d26b-43d3-b1d0-bda0700a3ea7)

### iv)Access rows and columns
```
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/37396662-5fef-445a-b4c4-0bf18fce40b5)

### v)Cut and paste portion of image
```
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/fc8d95b7-beb7-4d72-9930-0b3be5625b76)

### vi) BGR and RGB to HSV and GRAY
```
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
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/1255524e-2606-48cc-bd52-79e18d7b71bd)

![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/ba0288fe-a1a6-4659-b156-d101272ebe44)

### vii) HSV to RGB and BGR
```
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/4d5f83cc-0fb5-4b2c-8b93-6060a7a3d174)

### viii) RGB and BGR to YCrCb
```
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/89177b51-a2ad-4aeb-88e7-8352ebe54ea4)

### ix) Split and merge RGB Image
```
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
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/ca103bbd-dcb7-43c1-8996-248332638807)

### x) Split and merge HSV Image
```
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
#### OUTPUT
![image](https://github.com/NathinR/COLOR_CONVERSIONS_OF-IMAGE/assets/118679646/3049090b-f661-49e7-98b7-66c9e941a4a7)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







