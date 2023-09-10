# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
* i) Read, display, and write an image.
* ii) Access the rows and columns in an image.
* iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
```
Developed By: SASIDEVI V
Register No.: 212222230136
```
### Register Number: 
i) #To Read,display the image
```
import cv2
image=cv2.imread('dog.jpg',1)
image=cv2.resize(image,(400,300))
cv2.imshow('IMAGE',image)
cv2.waitKey(0)
```


Output:


![image](https://github.com/SASIDEVIvenaram/READ-AND-WRITE-IMAGE/assets/118707332/4636b30a-f48f-4fc1-b935-79325c0a0bd2)

ii) #To write the image
```
import cv2
image=cv2.imread('dog.jpg',1)
cv2.imwrite('new.jpg',image)
```
Output:


![image](https://github.com/SASIDEVIvenaram/READ-AND-WRITE-IMAGE/assets/118707332/f6c544fd-862b-429e-b6f7-ce43b14fb6d0)

iii) #Find the shape of the Image
```
print(image.shape)
```
Output:


![image](https://github.com/SASIDEVIvenaram/READ-AND-WRITE-IMAGE/assets/118707332/73060e6f-4422-4ea4-b582-f8926fd2c819)

iv) #To access rows and columns

```
import random
import cv2
image=cv2.imread('dog.jpg',1)
image=cv2.resize(image,(400,400))
for i in range(100):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
Output:

![image](https://github.com/SASIDEVIvenaram/READ-AND-WRITE-IMAGE/assets/118707332/4b7fa722-abbe-4872-b4a7-600a353647e2)

v) #To cut and paste portion of image
```
tag = image[300:400,300:400]
image[50:150,50:150] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
Output:



![image](https://github.com/SASIDEVIvenaram/READ-AND-WRITE-IMAGE/assets/118707332/3b160d5f-3b23-4e1f-9d5a-839a9c43d3c8)


## Result:
Thus the images are read, displayed, and written successfully using the python program.
