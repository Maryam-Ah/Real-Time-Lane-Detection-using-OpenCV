# Real-Time-Lane-Detection-using-OpenCV

Formulating the Problem Statement

The task that we wish to perform is that of real-time lane detection in a video. There are multiple ways we can perform lane detection. We can use the learning-based approaches, such as training a deep learning model on an annotated video dataset, or use a pre-trained model.

However, there are simpler methods to perform lane detection as well. In this article, I will show you how to do it without using any deep learning model. But we will use the popular OpenCV library in Python.

One thing we can do right away is to narrow down the area of interest. Instead of working with the entire frame, we can work with only a part of the frame. In the image below, apart from the lane markings, everything else has been hidden in the frame. As the vehicle would move, the lane markings would fall more or less in this area only:

What is a Frame Mask?

Here, a frame mask is nothing but a NumPy array. When we want to apply a mask to an image, we simply change the pixel values of the desired region in that image to 0, or 255, or any other number.

Image Pre-Processing for Lane Detection

We will first apply a mask to all the frames in our input video. Then, we will apply image thresholding followed by Hough Line Transformation to detect lane markings.

 

Image Thresholding

In this method, the pixel values of a grayscale image are assigned one of the two values representing black and white colors based on a threshold value. So, if the value of a pixel is greater than a threshold value, it is assigned one value, else it is assigned the other value.

Hough Line Transformation

Hough Transform is a technique to detect any shape that can be represented mathematically.



You can download the frames from this link: https://drive.google.com/file/d/1e4cc4zFFna3Owyym6aq7ZXoquHA2l95O/view
