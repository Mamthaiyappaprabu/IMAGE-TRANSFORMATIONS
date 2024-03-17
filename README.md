# IMAGE-TRANSFORMATIONS :

  
## Aim :
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

### Step1:
Import the required packages.
<br>
### Step2:
Load the image file in the program.
<br>

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
<br>

### Step4:
Display the modified image output.
<br>

### Step5:
End the program.
<br>

## Program:
### Developed By: MAMTHA I
### Register Number: 212222230076
### i)Image Translation :
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "FLOWER.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

### ii) Image Scaling :
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("DOG.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```


### iii)Image shearing :
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("NATURE.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()

```

### iv)Image Reflection :
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("PEACOCK.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  

```


### v)Image Rotation :
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("PANDA.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```

### vi)Image Cropping :
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("ROSE.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()

```
## output:
***1.Image Translation :***



![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/6940d1b8-2c86-4b9b-8796-f3aa48d944f6)    
![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/dbb7e9c0-5a2a-4236-9f3c-3c8f82bb1809)



 ***2.Image Scaling :***


 
 ![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/86b892f7-0b1a-4663-9806-c595587b3148)

 
 ***3.Image shearing :***


 
 ![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/d157e714-aad3-40e6-a700-1ab99a5a6ae2) 

 
 ![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/08664147-a59b-4067-aa18-a008c0064146)


 
 ***4.Image Reflection :***

 
 ![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/a40102d6-ca04-45d6-9990-9161c8010c22)

 
 ![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/9ab1d5ec-6fa6-413f-a0d0-154d2339d723)


 
 ***5.Image Rotation :***

 
 ![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/79fc13ee-9fcd-4fdc-8dee-0ee6ed2a46e5)

 
 ***6.Image Cropping :***

![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/84bf9a60-542d-48ad-88bf-8d1f50a3e146)


![image](https://github.com/Mamthaiyappaprabu/IMAGE-TRANSFORMATIONS/assets/119393563/871a49f2-6fca-4935-81c9-76de62c87aaa)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
