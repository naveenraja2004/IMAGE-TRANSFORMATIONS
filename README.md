# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>Import all the necessary modules

### Step2:
<br>Choose an image and save it as filename.jpg

### Step3:
<br>Use imread to read the image

### Step4:
<br>Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:
<br>Use cv2.warpPerspective(image,M,(cols*2,rows*2)) to scale the image
### Step6:
Use cv2.warpPerspective(image,M,(int(cols*1.5),int(rows*1.5))) for x and y axis to shear the image

### Step7:
<br>Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image
### Step8:
<br>Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image
### Step9:
<br>Crop the image to remove unwanted areas from an image
### Step10:

<br>Use cv2.imshow to show the image
### Step11:
<br>End the program
## Program:

## Developed By: NAVEEN RAJA N R
# Register Number:212222230093
i)Image Translation
```python

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread("dip.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()

```


ii) Image Scaling
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()
```


iii)Image shearing
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```

iv)Image Reflection
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```


v)Image Rotation
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
```


vi)Image Cropping
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('dip.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Cropping:")
plt.imshow(translated_image)
plt.show()
```




## Output:
 i)Image Translation

![image](https://github.com/Goutham2306/IMAGE-TRANSFORMATIONS/assets/138971154/5eb202eb-f87c-413c-8441-bf4fc765557d)




 ii) Image Scaling

![image](https://github.com/Goutham2306/IMAGE-TRANSFORMATIONS/assets/138971154/2e146ac8-3205-49c5-8232-4e74cc6c19df)





 iii)Image shearing

![image](https://github.com/Goutham2306/IMAGE-TRANSFORMATIONS/assets/138971154/44f107c7-36bd-4bf5-94b7-93ce96455eeb)





 iv)Image Reflection

![image](https://github.com/Goutham2306/IMAGE-TRANSFORMATIONS/assets/138971154/4309a747-ccff-49b8-93d8-ec296c3a5796)





 v)Image Rotation

![image](https://github.com/Goutham2306/IMAGE-TRANSFORMATIONS/assets/138971154/16e9c982-7316-4e58-ae21-11e786bcd714)






vi)Image Cropping

![image](https://github.com/Goutham2306/IMAGE-TRANSFORMATIONS/assets/138971154/06686662-5b58-4180-8c96-124800b23204)







## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
