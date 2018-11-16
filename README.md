# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />


Pipeline description:
1) Define the input vales:

| Variables        		|     Values        					| 
|:---------------------:|:---------------------------------------------:| 
| Lower Canny Edge filter thresholds         		|  		Lower=100, Upper=150				| 
| Gaussian Blur 	| kernel=3	|
| Vertical fraction 	| 40%	|
| Hough Tranform |  rho = 2 , theta = np.pi/180 ,threshold = 15 , min_line_len =40,max_line_gap =20     |
