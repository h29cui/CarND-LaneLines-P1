# **Finding Lane Lines on the Road** 

## Writeup

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

There are five steps in my pipeline:
1. convert the images to grayscle
2. remove gaussion noise from the images
3. canny edge detection
4. define region of interest
5. draw detected lanes 


In order to draw a single line on the left and right lanes, I modified the draw_lines() function by separately storing left lanes and right lanes into two different arrays. Then, averaging slopes and intecepts in each array. The final lanes are drawn based on the averaged result.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be the impact of an outlier line. For example, if there is a relatively long horizontal line in the middle of the road, it would be noisy to current lane detection because its slope and intecept values are outliers. 


### 3. Suggest possible improvements to your pipeline

A potential improvement would be eliminating outliers when averaging slopes and intecepts of the lines.
