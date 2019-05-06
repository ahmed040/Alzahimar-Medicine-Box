# Alzahimar-Medicine-Box
The purpose of this project is to use face detection feature provided by open CV along with image processing techniques to detect our special cup in order to insure the  patient receives his medicine pill on time. 
The algorithm used for cup detection is the bitwise "and" of dilated positive and negative threshed images.  
Because our unique cup has small white and black squares,  dilation of each threshold image will produce a white area in almost the exact position.  
After performing the bitwise "and" and several other processes, the back ground objects disappear and only the cup remains.  
The remaining cup is segmented and contoured; this contour is used to detect intersection of the cup with the square surrounding the face position.
once this condition is detected, a message is sent serially to arduino to indicate  the pills have been taken.
