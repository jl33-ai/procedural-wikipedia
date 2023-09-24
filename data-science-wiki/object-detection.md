# Object Detection Tutorial 👁️
Created by @jl33-ai 👦🏻

This notebook covers a beginner-friendly tutorial on Object Detection. Let's dive in! 🌊

## Table of Contents 📘
1. [Introduction to Object Detection](#intro)
2. [Object Detection Models](#models)
3. [Model Implementation](#implementation)
4. [Model Evaluation](#evaluation)
5. [Conclusion](#conclusion)

<a name='intro'></a>
## 1. Introduction to Object Detection 🔎

Object detection is a computer vision technique for locating instances of objects in images or videos. It can not only classify the type of object, but also accurately express the location of the object in the form of a bounding box or a pixel-by-pixel mask. Real-world applications include object tracking, surveillance, image retrieval and more. 

<a name='models'></a>
## 2. Object Detection Models 🏛️
- **Two-Stage Detectors** 👯‍♂️
    - _R-CNN_
        - Proposes regions and uses a CNN to classify the object in the region.
    - _Fast R-CNN_
        - Improves speed by sharing computation of the convolutional layers across different proposals.
    - _Faster R-CNN_
        - Uses a Region Proposal Network to share the convolutional layer with region proposal computation.
- **Single-Stage Detectors** 🕺
    - _YOLO_
        - Divides the image into a grid and predicts bounding boxes and class probabilities for each grid cell.
    - _SSD_
        - Discretizes the output space of bounding boxes into a set of default boxes over different aspect ratios and scales.
   
<a name='implementation'></a>
## 3. Model Implementation 💻

Python is widely used for implementing object detection models due to its extensive variety of libraries. Here, we use the imageai library with the YOLO model.

```python
from imageai.Detection import ObjectDetection

detector = ObjectDetection()
detector.setModelTypeAsYOLOv3()
detector.setModelPath(path_to_your_model)
detector.loadModel()
detections = detector.detectObjectsFromImage(input_image, output_image)

for eachObject in detections:
    print(eachObject["name"], " : ", eachObject["percentage_probability"]) 
```

<a name='evaluation'></a>
## 4. Model Evaluation 📏

For evaluating object detection models, metrics such as Precision, Recall, F1-score and Intersection over Union (IoU) are used commonly.

- _Precision_: True Positives / (True Positives + False Positives)
- _Recall_: True Positives / (True Positives + False Negatives)
- _F1-score_: Harmonic mean of Precision and Recall
- _IoU_: Intersection of bounding boxes / Union of bounding boxes

<a name='conclusion'></a>
## 5. Concluding Remarks 🎯 

In this notebook, we walked through the basics of object detection from understanding what it is, exploring some of the models and earlier approaches, and implementing a simple object detection model using the imageai library with Python.

Keep exploring and happy detecting! 🚀