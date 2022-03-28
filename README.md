# YOLOv3 
## Implement real-time object detection with YOLOv3 using OpenCV

Tried simulating real-time object detection with YOLOv3 architecture with the help from OpenCV tutorials

YOLOv3 object detector was pretrained with coco dataset, and you can download these files in the following link: https://pjreddie.com/darknet/yolo/

Below video is the output video of yolo_video.py with one of my videos recored with iphone.

https://user-images.githubusercontent.com/82307352/159221817-5bd791f4-49d8-4d2b-a051-6c9f7edc116f.mp4

Few minor notations regarding the codes yolo.py & yolo_video.py:

1. OpenCV module with version **_higher than 3.4.1_** is required to run the codes.
2. In yolo_video.py, I added lines 57 and 58 to circumvent the following error: CV2 Image Error: error: (-215:Assertion failed) !ssize.empty() in function 'cv::resize'
3. For both codes, I changed the code from "ln = [ln[i[0] - 1]" for i in net.getUnconnectedOutLayers()]" to "ln = [ln[i-1]  for i in net.getUnconnectedOutLayers()]". The former one didn't work for me (I guess it depends on which version of OpenCV you are using)
