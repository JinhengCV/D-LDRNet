# D-LDRNet
This open access dataset and official code is publicly available for our paper work "D-LDRNet: Monocular vision framework for all-weather safe ranging monitoring of vehicle in transmission lines". 

## Abstract
Efficient monitoring and early warning of hazards on transmission lines are crucial for the safety of both the lines themselves and the surrounding personnel. Among them, the monitoring for the real-time distance of construction machinery and other vehicles approaching power lines is an effective and cost-efficient method of hazard detection. This paper proposes a novel architecture named D-LDRNet for all-weather distance monitoring based on monocular vision, which can obtain three-dimensional information of hazardous objects using only a monocular camera. Firstly, an innovative feature extraction network is constructed to reduce redundant convolutional calculations and parameters, coupled with new upsampling operators and optimized detection head networks using Involution. Then, an improved low-light enhancement network is introduced to enhance the recognition performance of the detection model in nighttime scenarios. Finally, leveraging the pose matching relationship between images and point clouds, a ranging module for hazardous objects is designed and integrated into the constructed hazard detector. Experimental results conducted on surveillance images from different transmission line scenarios demonstrate that D-LDRNet not only possesses a more lightweight network structure but also exhibits optimal hazard detection performance in nighttime construction scenes. Experiments conducted on surveillance videos further confirm the effectiveness of the proposed ranging scheme and its industrial application significance.

<p align="center">
<img src="./video.gif" width="600"/>
</figure> 
</p>

## Methodology
The model architecture is shown as follow:

<p align="center">
<img src="./D-LDRNet.png" width="600"/>
</figure> 
</p>

## datasets
Our recording platform is a commercial autonomous surface vehicle. The platform adopts a deployable sensor configuration and is equipped with four surrounding cameras, a front-view LiDAR, six surrounding millimeter-wave radars, and an inertial navigation system (INS). The sensor setup of our platform is also illustrated in Figure. 2. The LiDAR and MMW radar systems provide accurate location measurements for the surrounding water surface system. With respect to camera configuration, we equipped 120° pinhole RGB cameras on the front view and back view of our recording platform, and each side of the boat is equipped with a fisheye camera for a high field of view. The detailed information about WSBEV dataset is described as follows:

### Data structure

```
- datasets
  - train
      - images
        - XXX.jpg
      - labels
        - XXX.txt
  - val
      - images
        - XXX.jpg
      - labels
        - XXX.txt
  - test
      - XXX.jpg
  - point cloud
```

## Visualization Samples
<p align="center">
<img src="./fig/3.png" width="600"/>
</figure> 
</p>
