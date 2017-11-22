# **Finding Lane Lines on the Road** 

**Finding Lane Lines on the Road**

The goal of the proejct is to create a pipeline that detects lanes in a a set of still images and video clips. The idea is to create this pipeline robust enough to variations for lane color and curve.

In my developed pipeline, I followed the following steps:

1. Convert the image to grayscale
2. Blur the grayscales image
3. Detect edges using canny edge detection
4. Create mask that filters out anything outside of a pre-defined region of interest
5. Use Hough to detect and draw lines on the images/clips

Initially I ws trying to filter white and yellow colors of the image and run the pipeline only on these masked images. But somehow the results without the mask was better. The color masked created more noise than anticipted. 

One of the biggest improvements could be to have a dynamic region of interest by using other type of data or information. The static region of interest causes issues in cases when there are vehicles and trucks in the image. If sensor information could be used to detect the ground and only search for lanes on the ground, the performance and robustness would increase.
