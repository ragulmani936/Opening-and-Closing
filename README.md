# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages.

### Step2:

Create the Text using cv2.putText.

### Step3:

Create the structuring element.

### Step4:

Use Opening operation.

### Step5:

Use Closing Operation.

### Step6:

Print the output and end the program.

 
## Program:

~~~
Developed by: Ragul M
Reg no:212221230080
~~~
~~~
# Import the necessary packages

import numpy as np
import matplotlib.pyplot as plt
import cv2


# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"Ishwarya.V",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image)
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation

opening_image = cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image)
plt.axis('off')


# Use Closing Operation

closing_image = cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image)
plt.axis('off')

~~~

## Output:

### Display the input Image

![img1](https://github.com/ragulmani936/Opening-and-Closing/blob/main/img1.png)

### Display the result of Opening

![img2](https://github.com/ragulmani936/Opening-and-Closing/blob/main/img2.png)

### Display the result of Closing

![img3](https://github.com/ragulmani936/Opening-and-Closing/blob/main/img3.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
