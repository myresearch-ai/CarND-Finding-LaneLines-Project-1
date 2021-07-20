# **Finding Lane Lines on the Road** 
![laneLines_thirdPass](https://user-images.githubusercontent.com/76077647/126323080-50adde24-93a3-4c49-a2a1-9a9a6657a413.jpg)

Overview
---

**Perception** is a fundamental requirement of any **autonomous system**. In order to successfully navigate the world (environment), an autonomous system - a self-driving car in this application - must be capable of perceiving its surroundings such as lane lines, road curves, pedestrians, etc. **Computer vision** techniques are used to achieve this goal - perception. Images & videos from cameras & other sensors are used as inputs in the computer vision system which is deigned to extract useful features to allow a self-driving car perceive its environment. 

Goal
---

The goal of this project is to develop a computer vision pipeline for detecting lane lines in images & videos from cameras using Python & OpenCV - a package that provides several useful computer vision tools.

Steps
---

To accomplish the intended goal, I developed a pipeline consisted of the following steps:

* Ingest images or videos in and apply preprocessing (gray scaling for images).
* Define a Kernel size & apply gaussian smoothing.
* Apply Canny transform to extract image edges (define our params for canny transform).
* Apply masking to the images (keep ROI).
* Run Hough-transform on masked images (using our params).
* Draw line segments.
* Extrapolate segmented lines above in step 6.
* Evaluate the accuracy of line annotations.

Several helper functions were used to implement these subroutines. Some functions provided by Udacity were adapted to fit processing images or videos to accomplish the goal.

Future Improvements
---

The pipeline performs well detecting straight lane lines. Applying it to the optional challenge problem reveals the current implementation's weakness - failure to accurately perceive curved lane lines. Future implementations will improve upon this weakness with more complex features. 


**Credits**

https://github.com/alkasm/SDCND-Project-1
