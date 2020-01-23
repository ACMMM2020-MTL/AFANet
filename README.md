# AFANet

  Implemention of Paper：Deep Adaptive Feature Aggregation in Multi-task Convolutional Neural Networks   
  
## Introduction
  ![](https://github.com/IJCAI2020-MTL/AFANet/raw/master/Architecture.png)   
  The Adaptive Feature Aggregation (AFA) layer for multi-task CNNs, in which a dynamic aggregation mechanism is designed to allow each task adaptively determines the degree to which the feature aggregation of different tasks is needed. We introduce two types of aggregation modules to the AFA layer, which realize the adaptive feature aggregation by capturing the feature dependencies along the channel and spatial axes, respectively.   
  
## Models
  * /models/`pixel_single.py` & `image_single.py`: single task baseline   
  * /models/`pixel_hard.py` & `image_hard.py`: parameters hard sharing baseline   
  * /models/`pixel_cross.py` & `image_cross.py`: cross stitch baseline   
  * /models/`pixel_nddr.py` & `image_nddr.py`: nddr-cnn baseline   
  * /models/`pixel_AFA.py` & `image_AFA.py`: our method   
  
## Requirements  

  Python >= 3.6  
  numpy  
  PyTorch >= 1.0  
  torchvision >= 0.2   
  tensorboardX  
  
## Installation
  1. Clone the repo:   
    ```
    git clone https://github.com/IJCAI2020-MTL/AFANet.git   
    ```   
    ```
    cd AFANet
    ```
  2. For custom dependencies:   
    ```
    pip install matplotlib tensorboardX   
    ```

## For Training   
  1. Configure your dataset path in `Dataloader.py`.   
  2. Deeplabv3+ networks with ResNet backbone are used to train semantic segmentation and depth prediction(see full input arguments in    ```train_multi.py``` ):   
    ```
    python train_multi.py
    ```


