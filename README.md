# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)


## My pipeline consisted of 7 steps:

1) Convert the images to grayscale
2) Apply Gaussian Smoothing
3) Apply Canny edge detection
4) Mask the image using the region of interest

![imagen](https://user-images.githubusercontent.com/41348711/48666377-b371cc00-eac0-11e8-9442-f532238effb7.png)

5) Create a blank to draw the lines on
6) Apply Hough lines filter to the masked image
7) Apply Hough lines filter to the masked image

For the first part of the project I used the function "draw_lines". According to the images already processed, slopes are inside the ranges 0.5 to 0.8 for the right side lines and -0.5 to -0.8 for the left side lines, so this will be used as a filter.
For the second part of the project (improve draw lines function) I built a new function called "draw_complete_lines".As every line is defined by a slope and x coordinate at the bottom of the image,median slope and median x coordinate are calculated for all the lines of each video frame of the video (with the slopes inside the ranges defined).
An array is set to save previous slopes and x coordinate values. As the change from
frame to frame in the video must be low and there is some noise I just used the
previous value and added just 10% of the increment from frame to frame.
I completed the code in order to cover all possible cases.

## Potential shortcomings

The weak point are the changes on lighting  (e.g. on the challenge file)




Pipeline description:
1) Define the input vales:

| Variables        		|     Values        					| 
|:---------------------:|:---------------------------------------------:| 
| Lower Canny Edge filter       		|  	Thresholds:	Lower=100, Upper=150				| 
| Gaussian Blur 	| kernel=3	|
| Vertical fraction 	| 40%	|
| Hough Tranform |  rho = 2 , theta = np.pi/180 ,threshold = 15 , min_line_len =40,max_line_gap =20     |
| Weight image	|     α=0.8 , β=1. , γ=0. |
