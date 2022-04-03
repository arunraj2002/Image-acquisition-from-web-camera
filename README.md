# Image-Acquisition-from-Web-Camera
## Aim
 
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
import cv2 and capture the video using cv2.VideoCapture(0)

### Step 2:
Write the captured image using cv2.imwrite("Arun.jpg",frame)

### Step 3:
Resize the image using cv2.resize(frame,(0,0),fx = 0.5,fy=0.5)

### Step 4:
Display the image untill the loop gets over

### Step 5:
Rotate the image using cv2.rotate(smaller_frame,cv2.cv2.ROTATE_180)

## Program:
``` Python
### Developed By: Arunraj.R
### Register No:212220230004

## i) Write the frame as JPG file
 import cv2

videoCaptureObject = cv2.VideoCapture(0)

ret,frame = videoCaptureObject.read()
cv2.imwrite("NewPicture.jpg",frame)

videoCaptureObject.release()
cv2.destroyAllWindows()



## ii) Display the video
import cv2
import numpy as np

cap = cv2.VideoCapture(0)


while True:
    ret, frame = cap.read()

    cv2.imshow("NewPicture",frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

videoCaptureObject.release()
cv2.destroyAllWindows()



## iii) Display the video by resizing the window
import cv2
import numpy as np

cap = cv2.VideoCapture(0)


while True:
    ret, frame = cap.read()
    width = int(cap.get(3))
    height = int(cap.get(4))
    
    image = np.zeros(frame.shape, np.uint8)
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)

    cv2.imshow("NewPicture.jpg",smaller_frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

videoCaptureObject.release()
cv2.destroyAllWindows()




## iv) Rotate and display the video

 import cv2
import numpy as np

cap = cv2.VideoCapture(0)

while True:
    ret, frame = cap.read()

    frame = cv2.rotate(frame,cv2.cv2.ROTATE_180)

    cv2.imshow("NewPicture.jpg",frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

videoCaptureObject.release()
cv2.destroyAllWindows()







```
## Output

### i) Write the frame as JPG image
![Screenshot (372)](https://user-images.githubusercontent.com/75235747/161419608-84078450-d0e6-4280-a25a-a9032daaf5f5.png)



### ii) Display the video
![Screenshot (372)](https://user-images.githubusercontent.com/75235747/161419618-1bd200fb-7bd1-46ef-864f-f775feb893a3.png)



### iii) Display the video by resizing the window
![Screenshot (373)](https://user-images.githubusercontent.com/75235747/161419629-b2ce1c88-ede3-4309-947c-77c9328d6312.png)




### iv) Rotate and display the video
![Screenshot (375)](https://user-images.githubusercontent.com/75235747/161419633-5eef0a12-f594-4d84-a14d-a0935db0eca3.png)






## Result:
Thus the image is accessed from webcamera and displayed using openCV.
