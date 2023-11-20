# YOLOv8-Improved-Pose-Estimation
YOLOv8 is a highly innovative algorithm, where [Pose estimation](https://docs.ultralytics.com/tasks/pose/) is a research field in computer vision, a subdomain of artificial intelligence. It focuses on automatically detecting and analyzing the postures and positions of humans or animals in images or video clips. When the goal is to determine whether it's one or multiple objects, it identifies the nodes of various joints. This technology has a wide range of applications, from sports analysis, Virtual Reality, health monitoring, to monitoring worker safety and improving process management.

However, due to factors such as complex body movements or environmental conditions, it is common for the key points of the human body's pose to extend beyond the body's boundaries. When merely recognizing the sequence of poses (such as requiring only the x and y-axis coordinates), the impact is relatively small. However, when using a depth camera for distance measurements of these nodes, it can result in significant distance inaccuracies.
Therefore, this experiment aims to address this issue and improve it so that all key points are accurately constrained within the human body.

## YOLOv8
[Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics) is a cutting-edge, state-of-the-art (SOTA) model that builds upon the success of previous YOLO versions and introduces new features and improvements to further boost performance and flexibility. YOLOv8 is designed to be fast, accurate, and easy to use, making it an excellent choice for a wide range of object detection and tracking, instance segmentation, image classification and pose estimation tasks.

## Features
Through the use of a for loop, we can obtain each key point of the human body's pose one by one. We calculate the distances between each pair of coordinates, and use statistical methods like [Quartile](https://en.wikipedia.org/wiki/Quartile) to identify and handle outlier values. Finally, for the coordinates corresponding to these outlier values, we perform calculations to determine the appropriate adjustments. This approach helps address the issue of key points extending beyond the body's boundaries and enhances the accuracy of pose estimation.
  
### Results
| Yellow dots indicate correction values. | Purple dots indicate correction values |
| ------------- | ------------- |
| ![ky](https://github.com/KennyChen880127/YOLOv8-Improved-Pose-Estimation-Code/assets/99500847/736297f3-c182-4e9e-82d8-0c089b2e57b8) | ![home](https://github.com/KennyChen880127/YOLOv8-Improved-Pose-Estimation-Code/assets/99500847/15fd064e-14a4-496b-b576-806514fb436b) |
