# **Writeup Report Project 1: Finding Lane Lines on the Road**

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./images/solidWhiteCurve_out.jpg "Output image"
[image2]: ./images/solidWhiteCurve_out_imp.jpg "Output image improved"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps.  
  First, I convert the image to grayscale.  
  Second, I use "Canny Edge Detection" to the grayscale image.  
  Third, I cut off the triangle region with two lane lines.  
  Fourth, I use "Hough Transform" and find the lane lines from the previous image.  
  Fifth, I draw red lines as detected lane lines on the original image.  

In fourth step, the found lines are not perfect lines if lane lines are dotted lines. In order to draw lines in this case, I used the least squares method in draw_lines() function and detected fitting lines.

![alt text][image1]

![alt text][image2]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ...

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
