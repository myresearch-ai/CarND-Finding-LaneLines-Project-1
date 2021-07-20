# Self-Driving-Car-ND-Project-1
This project is the first in the self driving car nanodegree offered by Udacity. 

![line-segments-example](https://user-images.githubusercontent.com/76077647/126308756-2462379a-5cbb-4a71-8d04-a839e8b89246.jpg)

### 1. Overview

**Percecption** is a fundamental requirement of any **autonomous** system - a car in this application. In order to successfully navigate the world such as be able to follow lanes, take turns, determine appropriate trajectory,etc., the autonomous car must be capable of **perceiving the world around** it. **Computer vision** techniques are used to achieve the self-driving-car's ability to **perceive the world**. 

In this project we will detect lane lines in images & vides from cameras using Python & OpenCV - a library that provides several useful computer vision tools for analyzing images & videos. 

### 2. Pipeline

The goal of this project is to make a pipeline that finds lane lines on the road. This pipeline is consisted of the following steps:

* Ingest images & apply gray scaling
* Define a Kernel size & apply gaussian smoothing
* Apply Canny transform to get image edges (define our params for canny transform)
* Apply masking to the images (keep ROI)
* Run Hough-transform on masked images (using our params)
* Draw line segments
* Extrapolate segmented lines above in step 6
* Evaluate the accuracy of line annotations

Several helper functions were provided to implement these steps - a few of these functions had to be modified as fit. After the initial implemetation & testing of the pipeline over test images, the pipeline was then applied to videos.

### 3. Possible Improvements

The current implementation performs well as long as lanes are straight. As demonstrated in the last application of the pipeline to a curved section of the road (optional challenge), the car fails to accurately perceive lanes. This reveals a weakness of this implementation which will be solved in later projects that are complex enough. 
