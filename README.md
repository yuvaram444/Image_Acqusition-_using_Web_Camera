
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
<br>Use cv2.VideoCapture(0) to access web camera

### Step 2:
<br>Use cv2.imread to read the video or image

### Step 3:
<br> Use cv2.imwrite to save the image

### Step 4:
<br> Use cv2.imshow to show the video

### Step 5:
<br> End the program and close the output video window by pressing 'q'.

## Program:
``` Python```
### Developed By:YUVARAM S
### Register No: 212224230315

## i) Write the frame as JPG file
```import cv2
videoCaptureObject = cv2.VideoCapture(0)
ret, frame = videoCaptureObject.read()
if ret:
    cv2.imwrite("sanjay.jpg", frame)
videoCaptureObject.release()
cv2.destroyAllWindows()
```
## ii) Display the video
```import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('Harish',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230045-Harish',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
```import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230045-Harish',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
</br>

![Screenshot 2025-04-06 122241](https://github.com/user-attachments/assets/7c70ad82-ea38-4729-b395-8971d5340e2b)

</br>



### ii) Display the video
</br>

![Screenshot 2025-04-06 122335](https://github.com/user-attachments/assets/3c441321-7555-46dc-b34d-8b41ee04b2ec)

</br>


### iii) Display the video by resizing the window
</br>

![Screenshot 2025-04-06 122727](https://github.com/user-attachments/assets/694eb360-29b6-48a3-a378-df9d0a66c0c0)

</br>



### iv) Rotate and display the video
</br>

![Screenshot 2025-04-06 122923](https://github.com/user-attachments/assets/409b1bed-bc5d-4fb3-b0a4-882886892fa8)

</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
