# Finding lane lines

## Project 1 for Udacity Self-Driving Car Nanodegree

This is a project I created for the Udacity Self-Driving Car Engineer Nanodegree. The goal was to build a pipeline of image processing functions that takes a road image / video as input and outputs the image / video with lane lines marked with straight red lines.

<p align="center">
  <img src = "https://github.com/gyadam/finding-lane-lines/raw/master/images/output.png" width="480">
<p align="center">
  
The entire code is available in this repository in a [Jupyter notebook](https://github.com/gyadam/finding-lane-lines/blob/master/FindingLaneLines.ipynb) which includes code to test the pipeline with an image and a video.
The output video is available on YouTube:
https://youtu.be/Mh9md_DV30o

## Pipeline

The pipeline consists of 7 steps:
- Conversion to grayscsale
- Gaussian blur
- Canny edge detection
- Selection of region of interest
- Hough transformation
- Extrapolation of the Hough lines
- Adding the lane lines to the original image

The functions are implemented using the *OpenCV*, *NumPy* and *matplotlib* libraries. The pipeline is demonstrated below with the outputs of each step:

Original image:

![alt text](https://github.com/gyadam/finding-lane-lines/blob/master/images/original.png)

After grayscale conversion:

![alt text](https://github.com/gyadam/finding-lane-lines/blob/master/images/grayscale.png)

Gaussian blur applied:

![alt text](https://github.com/gyadam/finding-lane-lines/blob/master/images/blurred.png)

Image after Canny edge detection:

![alt text](https://github.com/gyadam/finding-lane-lines/blob/master/images/edges.png)

Cropped according to "region of interest" mask:

![alt text](https://github.com/gyadam/finding-lane-lines/blob/master/images/masked_edges.png)

Hough transformation (pixels -> lines):

![alt text](https://github.com/gyadam/finding-lane-lines/blob/master/images/raw_lane_lines.png)

Extrapolating the lines:

![alt text](https://github.com/gyadam/finding-lane-lines/blob/master/images/full_lane_lines.png)

Final result:

![alt text](https://github.com/gyadam/finding-lane-lines/blob/master/images/output.png)

