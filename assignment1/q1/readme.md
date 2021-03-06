# Data Management - Line Dataset Generation

## Problem Statement

Make a dataset of (28×28×3) images ofstraight lineson ablack background with the following variations:
1. Length- 7 (short) and 15 (long) pixels.
2. Width- 1 (thin) and 3 (thick) pixels.
3. Angle with X-axis- Angle θ∈[0,180) degree at intervals of 15 degree.
4. Color- Red and Blue.

## Solution
We have  used four python libraries for this solution.
1. numpy
2. opencv
3. pillow
4. os

#### numpy
To create an image, we have used numpy array.

#### opencv
To create a video from images, we have used opencv.

#### pillow
To save the image generated by numpy array, we have used pillow.

#### os
To create directories and create/delete files

### Functions
1. `create_img(originx, originy, angle, len, color, thick)`
2. `build_video(img)`

#### `create_img()`
This funtion takes origin, angle with x axis, length of line, color of line and thickness as parameters and returns (1, image array) if image is possible or returns (0, default) if image is not possible for given parameters.

#### `build_video()`
This function takes image array as parameter. After 9 images, it constructs one image of those 9 images and write it in videowriter.

### Global
First, we have initialized video writer using opencv. We have used 4 nasted `for` loops to construct images of one class. Each class again has 2 masted for loops for deciding orogin. Then, we call `create_img()` function with parameters according to classes and origin. The image array returned by `create_img()` is getting saved as a file using PIL and it is also passed in `build_video` if the image is one of first 90 images fir each class.

## Files Location
- Code - ./q1.py
- Images - ./images/
- Video - ./video/video.avi
- Notebook - ./q1_notebook.ipynb
