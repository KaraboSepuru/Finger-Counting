# Finger-Counting
Count the number of fingers on a colour image of a cropped hand. Your output should be the number of fingers held up

# Introduction
Finger counting, also known as finger detection or hand gesture recognition, plays a vital role in various human-computer interaction applications. The ability to accurately count the number of fingers held up in a hand image has practical significance in fields
such as virtual reality, robotics, and sign language interpretation. We aim to develop a robust and efficient solution for finger counting by utilizing non-learning-based image processing techniques. 

This project focuses on applying non-learning techniques to count the number of fingers in a color image of a cropped hand. We explore using digital image processing algorithms and methods to detect and quantify the fingers held up in the hand image. We aim to develop an effective solution that can handle varying hand orientations, shapes, and sizes by leveraging image enhancement, segmentation, and contour analysis techniques.

# Dataset
The dataset used in this project was obtained from Kaggle, featuring images of left or right hands with categorized finger counts (0 to 5). It offers diverse hand orientations, shapes, and sizes, ensuring a realistic representation of finger-counting scenarios. Care was taken to maintain balance across finger count categories, minimizing bias. The dataset will be used to evaluate the proposed non-learning-based image processing techniques' performance.

# Approach Description
The finger-counting approach involves the following steps:
** Image Smoothing **: Apply a Gaussian filter to reduce noise and enhance image quality.
** Thresholding **: Use Otsu thresholding to convert the smoothed image into a binary image.
** Hole Closing **: Use morphological operations to close gaps in the hand region and make it solid.
** Contour Filtering **: Identify contours in the thresholded image (optional if one hand is assumed).
** Convex Hull and Defects **: Compute the convex hull (outer boundary) and defects (concave regions between fingers) of the hand contour.
** Finger Counting **: Analyze the hand contour and defects to count fingers accurately. Validate defects based on angles between adjacent fingers and their depth.
** Handling No-Finger and One-Finger Scenarios **: Use the hand contour area compared to the average palm area to differentiate between no-finger raised and one-finger raised cases.

These additional validation steps based on angle and depth improve the accuracy of finger identification and minimize miscounting. The approach handles various hand configurations and imaging conditions, making the finger-counting system more reliable.
