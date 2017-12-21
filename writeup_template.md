# **Finding Lane Lines on the Road** 

## Overview



**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Enhance the pipleline to average/extrapolate the line segments you detect to map out the full extent of the lane


<img src="./test_images/solidWhiteCurve.jpg" width="280" alt="Combined Image" /> <img src="./examples/line-segments-example.jpg" width="280" alt="Combined Image" /> <img src="./examples/laneLines_thirdPass.jpg" width="280" alt="Combined Image" />




### Reflection

### 1. The pipeline.

My pipeline consisted of 5 steps.

### Color selection

     
First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

### Region of interest selection
### Grayscaling
### Gaussian smoothing 
### Canny Edge Detection 
### Hough Tranform
### Draw Line (Draw_Line and Draw_Line_Ex)
     cv2.addWeighted() to coadd / overlay two images cv2.cvtColor() to grayscale or change color cv2.imwrite() to output images to file
     cv2.bitwise_and() to apply a mask to an image


### 2. Potential shortcomings with the current pipeline

  This approach is not resilient enought to handle the following conditions:
   - Shadows, Weather and Light condition
   - Curved lanes
   - Street imperfections (faded lanes)..


### 3. Possible improvements

A possible improvement would be to ...

   - Use different color selection to handle different lighting conditions.
   - Support other street markings.
   - Adaptive estimation of street lane based on historical data to compensate for  street imperfection (possibley using Kalman Filter - LQE)
