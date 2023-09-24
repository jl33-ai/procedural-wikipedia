# Data Augmentation in Machine Learning :chart_with_upwards_trend:
Created by @jl33-ai 👦🏻

Data Augmentation is a strategy that enables us to significantly increase the diversity of data available for training models, without actually collecting new data. This document will walk you through the different techniques used for data augmentation.

## Table of Contents :pushpin:
- [What is Data Augmentation?](##What-is-Data-Augmentation?)
- [Reasons to Use Data Augmentation](##Reasons-to-Use-Data-Augmentation)
- [Common Techniques Used for Data Augmentation](##Common-Techniques-Used-for-Data-Augmentation)
- [Data Augmentation in Action](##Data-Augmentation-in-Action)

## What is Data Augmentation? :question:

Data augmentation techniques include creating transformed versions of images in the dataset that you are working with. They can involve rotations, stretches, flips, and many more.

The theory behind this technique is to create a wider variation in the data you have to train with. 

## Reasons to Use Data Augmentation :point_right:
1. **To increase the data:** In some cases, we have very less data to train our model, in this scenario, we can use data augmentation to generate more data.
2. **To create a more robust model:** Since we're creating a variety of modified images, your model is likely to become more general and less overfitted to the specific data you have.

## Common Techniques Used for Data Augmentation :bar_chart:
Different types of Augmentation techniques used in Image data are as follows:
- **Flipping:** You can flip images either vertically or horizontally.
- **Rotation:** You can randomly rotate some training images by a certain degree.
- **Zooming:** You can randomly zoom into images.
- **Brightness:** Vary the brightness of the image.
- **Scaling:** You can perform random rescaling.
- **Cropping:** Randomly crop images at all directions.

With Non-Image types of Data, following are the few common techniques:
- **Random Noise Injection:** Adding noise randomly.
- **Sampling:** You take samples and then extrapolate it.
- **Dictionary Based:** A dictionary of synonyms for feature replacement.
  
## Data Augmentation in Action :running:

Let's use Python's Augmentor library for increasing our model's capability to understand a wider variety of images. Here's how you can do it.

```python
import Augmentor

p = Augmentor.Pipeline("path_to_your_images...")
p.rotate(probability=0.7, max_left_rotation=10, max_right_rotation=10)
p.zoom(probability=0.5, min_factor=1.1, max_factor=1.5)
p.flip_left_right(probability=0.5)
p.sample(10000)
```
After this, the augmented dataset is ready in the output directory where you can use it for your model training.

## Conclusion 🎯
Through this, we have learned about data augmentation and its techniques. If used correctly, these techniques can help us build better machine learning models by expanding the diversity of the data available for training, whether it be image or text.