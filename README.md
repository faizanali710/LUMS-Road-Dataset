# LUMS Road Dataset
 
This dataset was collected for my senior year project titled "Developing an AI-Powered Autonomous Delivery Vehicle For Efficient Last Mile Delivery" at the Lahore University of Management Sciences (LUMS). The objective of this project was to develop an ADV that can self-navigate its way across the LUMS campus roads. More can be read about this project in this [report](https://drive.google.com/file/d/1h10nqKdAF45nh_qeJYBRUZCC9tG98CAv/view).

## Introduction

Visual perception plays a critical role in the functionality of Autonomous Delivery Vehicles (ADVs), as they must accurately identify and differentiate between various objects in their environment. Achieving this requires real-time semantic segmentation, which we achieved by deploying our trained model on an NVIDIA Jetson Nano. The effectiveness of the segmentation model is dependent on its training with a robust and comprehensive dataset. To meet this requirement, we meticulously gathered and manually annotated an extensive dataset using the [RoboFlow](https://universe.roboflow.com/senior-project-irtnh/lums-road-dataset) platform.

## Dataset Details

The dataset consists of 5 classes:

- 0 - **background**
- 1 - **obstacle**
- 2 - **road**
- 3 - **sidewalk**
- 4 - **speedbreaker**

The original dataset consisted of 926 unique images. However, the dataset was increased to 2224 images after we applied the following augmentations to create 3 versions of each source image for increasing robustness:

* 50% probability of horizontal flip
* Randomly crop between 0 and 30 percent of the image
* Random rotation of between -15 and +15 degrees
* Random brigthness adjustment of between -25 and +25 percent
* Random exposure adjustment of between -15 and +15 percent
* Random Gaussian blur of between 0 and 2 pixels
* Salt and pepper noise was applied to 1.05 percent of pixels

Here's a sample image and its corresponding mask:

![sample](C:\Users\Faizan\Documents\GitHub\LUMS-Road-Dataset\sample_image.png)