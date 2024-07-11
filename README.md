In the recent times, there is increase in road accident due 
to various factors mainly due to human error. ADAS system is made 
to help driver in driving and thereby reduce accident caused by 
human error. It include various sub system which work together to 
assist driver. Lane detection is one such system in place to assist 
driver. It play an integral role in self- driving car. It detects the lane 
line and keep car align with it. Therefore, it is very important to have 
a precise and fast system and that can work any condition of road. 
In this paper, we achieve lane detection by reading the image, 
defining region of interest, cropping the image to retain only region 
of interest, and then identifying lane lines in the image.

-----------------------------------------------------------------Algorithm Used------------------------------------------------------------

Region of interest Masking:
--------------------------
Before edge detection and line 
detection, a region of interest (ROI) is defined to focus only on 
the area of the image where lane lines are expected. This helps 
reduce processing time and avoid detecting irrelevant lines 
outside the region of interest 

![image](https://github.com/archiii35/Lane-detection-project/assets/90090854/8993311d-ccfb-44b9-94bb-fd9ed5007483)
-- Real image



![image](https://github.com/archiii35/Lane-detection-project/assets/90090854/85c5a28a-dfaa-4dc0-bc22-8211427a05ae)
-- ROI


Canny Edge Detection: 
----------------------
This algorithm is used to recognise the 
numerous edges that may exist in photos. To work and detect 
edges, the Canny edge detector requires grayscale images as 
input. To use the canny edge detector, incoming video frames 
must be transformed to grayscale first. It uses four step 
process. Removal of noise in input image using a Gaussian filter. 
Computing the derivative of Gaussian filter to calculate the 
gradient of image pixels to obtain magnitude along x and y 
dimension. Considering a group of neighbors for any curve in a 
direction perpendicular to the given edge, suppress the non- 
max  edge  contributor pixel points. Considering a group of 
neighbors for any curve in a direction perpendicular to the 
given edge, suppress the non- max edge  contributor pixel 
points. Lastly, use the Hysteresis Thresholding method to 
preserve the pixels higher than the gradient magnitude and 
neglect the ones lower than the  low  threshold  value. 

![image](https://github.com/archiii35/Lane-detection-project/assets/90090854/b7519e6c-211c-46f1-9cbe-b34024c7578c)


Hough Transform: 
----------------
After edge detection, the Hough transform 
is applied to detect lines in the image. The Hough transform is a 
technique used in image processing to detect shapes, 
particularly lines or curves. In this case, it's used to detect 
straight lines that correspond to lane markings 
Line Drawing: After detecting lines using the Hough transform, 
the code draws these lines onto a blank image and overlays it 
on the original frame. This process highlights the detected lane 
lines for visualization 

![image](https://github.com/archiii35/Lane-detection-project/assets/90090854/b03d636a-eafe-4f89-8aaf-5fd0dda4f749)
Hough line forming.

Result
-------

![image](https://github.com/archiii35/Lane-detection-project/assets/90090854/c7dd2c1a-02ac-4b7e-aa9f-8bd451d198e0)

As seen in the above picture, the lanes have been successfully detected and hence been spotted by the model. This feature will help in enhancing the 
safety og the driver and the vehicle.

Conclusion--

A lane detection system was developed through extensive 
research, design, and planning. It can be used by autonomous 
driving systems to provide safer travel for passengers, 
pedestrians, and vehicles around. This model provide increased 
accuracy on detecting lines. The main advantage of this 
approach is that it requires no trained model to predict the lanes 
on the road. Rather it actively takes in the video frames as input 
and actively detects the edges in the frame which are then given 
back as lanes to the user. This is an advantage as no time is spent 
developing a dataset, training, and testing it. This system 
provides the user to quickly implement lane detection in their 
implementation of autonomous driving systems. 


