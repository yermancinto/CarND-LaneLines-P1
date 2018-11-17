# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

My pipeline consisted of 5 steps:

1) First, I converted the images to grayscale
2) Apply Gaussian Smoothing
3) Apply Canny edge detection
4) Mask the image using the region of interest

![imagen](https://user-images.githubusercontent.com/41348711/48666242-30e80d00-eabe-11e8-85bc-59ca0f736a75.png)

5) Create a blank to draw the lines on
6) Apply Hough lines filter to the masked image.

For the first part of the project I used the function "draw_lines":

![imagen](https://user-images.githubusercontent.com/41348711/48666286-f894fe80-eabe-11e8-8716-e49827fcd7fc.png)

According to the images already processed, slopes are inside the ranges 0.5 to 0.8 for
the right side lines and -0.5 to -0.8 for the left side lines, so this will be used as a filter.
For the second part of the project (improve draw lines function) I built a new function
called "draw_complete_lines":



If you'd like to include images to show how the pipeline works, here is how to include an image: 



Pipeline description:
1) Define the input vales:

| Variables        		|     Values        					| 
|:---------------------:|:---------------------------------------------:| 
| Lower Canny Edge filter       		|  	Thresholds:	Lower=100, Upper=150				| 
| Gaussian Blur 	| kernel=3	|
| Vertical fraction 	| 40%	|
| Hough Tranform |  rho = 2 , theta = np.pi/180 ,threshold = 15 , min_line_len =40,max_line_gap =20     |
| Weight image	|     α=0.8 , β=1. , γ=0. |
