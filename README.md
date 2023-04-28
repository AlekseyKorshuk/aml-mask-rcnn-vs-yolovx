# Comparison of Mask RCNN vs Yolovx

The goal of this assignment is train both models on custom annotated dataset. 

1. Take photos of your environment of two or more objects. (at least 100 instances between all objects) 

2. Annotate them on roboflow. 

3. Train a Mask RCNN model using detectron2

4. Train Yolov8 the smallest size

5. Evaluate both models based on mAP and speed and size.

# Colab notebook 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AlekseyKorshuk/aml-mask-rcnn-vs-yolovx/blob/main/AML_%7C_Mask_RCNN_vs_Yolovx.ipynb)

Follow this
link: [link](https://colab.research.google.com/github/AlekseyKorshuk/aml-mask-rcnn-vs-yolovx/blob/main/AML_%7C_Mask_RCNN_vs_Yolovx.ipynb)

# Taking photos

I desided to detect spoon and fox. So here are example images:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/fox.jpeg" alt="Fox" width="320"/><img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/spoon.jpeg" alt="Spoon" width="320"/>

# Annotation with roboflow

This is very easy to annotate obhject detection dataset. Here is a screenshot from the roboflow ui:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-mask-rcnn-vs-yolovx/main/docs/annotation.jpeg" alt="Annotation" width="1200"/>

# Faster RCNN using detectron2

Based on official documentation of detectron2 and roboflow I was able to train Mask RCNN with detectron2. 

Sample predictions:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-mask-rcnn-vs-yolovx/main/docs/rcnn.png" alt="preds" width="320"/>

# Yolov8

With the usage of yolo client it was super smooth to train yolov8s on custom dataset: 

Sample predictions:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-mask-rcnn-vs-yolovx/main/docs/yolo.jpg" alt="preds" width="1200"/>

# Comparison

- Mean Average Precision
  - Mask RCNN: 74.18%
  - Yolov8: 82.3%
- Speed:
  - Yolo is a lot faster and such speed gives a lot of betefits despite its size
  - Yolo training for 24 epochs done in 4 minutes, but Faster RCNN in 55 minutes
- Size:
  - Mask RCNN model size: 335.82 Mb
  - Yolov8 model size: 22.79 Mb

# Resources

- https://docs.roboflow.com
- https://blog.roboflow.com/how-to-train-detectron2/
- https://blog.roboflow.com/how-to-train-yolov8-on-a-custom-dataset/
- https://github.com/facebookresearch/detectron2
- https://ultralytics.com/yolov8
- https://blog.roboflow.com/detectron2-custom-instance-segmentation/
- https://roboflow.com/model/yolov8-instance-segmentation



