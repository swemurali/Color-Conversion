# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
## Step1:
Import cv2 and save an image as scolor.jpeg.

## Step2:
Use imread to read and display the image.

## Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

## Step4:
Split and merge the image using cv2.split and cv2.merge commands.

## Step5:
End the program and view the output image windows.

## Program:
```
python
# Developed By: M.Suwetha
# Register Number: 212221230112
# READ AND DISPLAY THE IMAGE
import cv2
scolor=cv2.imread('aa.jpeg')
cv2.imshow('Original Image',scolor)
cv2.waitKey(0)
cv2.destroyAllWindows()
# i) Convert BGR and RGB to HSV and GRAY
#BGR2HSV
hsvimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY
grayimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2HSV
hsvimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2GRAY
grayimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()


# ii)Convert HSV to RGB and BGR
#HSV TO RGB
rgbimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',rgbimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#HSV TO BGR
bgrimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',bgrimg)
cv2.waitKey(0)
cv2.destroyAllWindows()




# iii)Convert RGB and BGR to YCrCb
#BGR TO YCrCb
ybgr=cv2.cvtColor(scolor,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',ybgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB TO YCrCb
yrgb=cv2.cvtColor(scolor,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',yrgb)
cv2.waitKey(0)
cv2.destroyAllWindows()



# iv)Split and Merge RGB Image
# SPLIT AND MERGE RGB IMAGE

blue=scolor[:,:,0]
green=scolor[:,:,1]
red=scolor[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()



# v) Split and merge HSV Image
# SPLIT AND MERGE HSV IMAGE
hsv = cv2.cvtColor(scolor, cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("Gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()



```
## Output:
![p-1](https://user-images.githubusercontent.com/94165336/228330292-de86d0b8-b35f-4874-807b-2864e287c917.png)

### i) BGR and RGB to HSV and GRAY
![p-2](https://user-images.githubusercontent.com/94165336/228330303-33822af1-f6ff-42de-8970-cb00357deb31.png)
![p-3](https://user-images.githubusercontent.com/94165336/228330326-75a9c2f8-7e51-4f52-8a9d-9a2f8e05c86c.png)

### ii) HSV to RGB and BGR
![p-4](https://user-images.githubusercontent.com/94165336/228330411-8487cc51-e944-4719-a0ce-c7ad938c99b8.png)
![p-5](https://user-images.githubusercontent.com/94165336/228330515-fd4cb557-1394-4c4c-8107-8811e177f15f.png)

### iii) RGB and BGR to YCrCb
![p-6](https://user-images.githubusercontent.com/94165336/228330576-7f69d766-f0e6-4ca8-beb0-1332398ed45e.png)
![p-7](https://user-images.githubusercontent.com/94165336/228330605-2d30e89d-e5b6-4d53-84bb-bf49ad9b58b8.png)
![p-8](https://user-images.githubusercontent.com/94165336/228330647-768e2ea4-88da-488b-a697-a5371ceb1cec.png)
![p-9](https://user-images.githubusercontent.com/94165336/228330672-a9d14cee-0ddc-4c21-a6df-e12e35dc17bc.png)

### iv) Split and merge RGB Image
![p-10](https://user-images.githubusercontent.com/94165336/228330703-1bfbbf7a-91e8-49b5-b1b0-7915b5cba7a6.png)
![p-11](https://user-images.githubusercontent.com/94165336/228330733-2df3bfb9-2ead-4f84-b88a-3c08af4561bf.png)
![p-12](https://user-images.githubusercontent.com/94165336/228330752-7e8912aa-f81a-4730-a8a1-d5246cdda9d6.png)
![p-13](https://user-images.githubusercontent.com/94165336/228330771-bc661b88-2c99-4b17-90bf-4fdad2602609.png)


### v) Split and merge HSV Image
![p-14](https://user-images.githubusercontent.com/94165336/228330927-19ebbbe4-d963-4565-9321-bb59273a4f5d.png)

![p-15](https://user-images.githubusercontent.com/94165336/228330816-cccd95c5-726f-4d9c-bf4b-afd5bed2cfc3.png)
![p-15](https://user-images.githubusercontent.com/94165336/228330983-c631c18b-5bed-43f5-8479-8a4c4ecd08f9.png)

![p-16](https://user-images.githubusercontent.com/94165336/228330998-cde102ca-bf33-41a1-9a38-d69619ce01a8.png)
![p-17](https://user-images.githubusercontent.com/94165336/228331017-87eeb424-e61c-4583-b690-bb72fb963c6d.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
