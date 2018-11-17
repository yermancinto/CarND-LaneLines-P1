# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

My pipeline consisted of 5 steps:

1) First, I converted the images to grayscale
2) Apply Gaussian Smoothing
3) Apply Canny edge detection
4) Mask the image using the region of interest
5)

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

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
