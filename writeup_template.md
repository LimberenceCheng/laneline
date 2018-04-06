# **Finding Lane Lines on the Road** 

When we drive, we use our eyes to decide where to go and strictly obey the simple rules like stay between the lane lines. Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm. In this project I will detect lane lines in images using Python and OpenCV. I have average/extrapolate them and draw them onto the image then with the knowledge of that I applied the methods to the video stream.

### 1. Pipelines and How I draw the lines.

My pipeline consisted of 5 steps. 

1. Convert the image into gray scale.
2. Performing Gaussian blurring (smoothening) on the gray scale image.
3. Canny edge detection on the blurred image.
4. Define region of interest and mask out portion of the image.
5. Apply Hough transform.

The first step in the lane detection pipeline is to convert the color image with dimension of WxH*3 (where W is width and H is hight and 3 the color(RGB) or depth of the image) into gray scale image of dimension W*H*1. This process helps us to identify edges based of difference in brightness of neighboring pixels(i.e by computing the gradient , ($df/dx$,df/dy) ).So I have used `grayscale = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)` to solve the problem. The function converts an input image from one color space to another. In case of a transformation to-from RGB color space, the order of the channels should be specified explicitly (RGB or BGR). Note that the default color format in OpenCV is often referred to as RGB but it is actually BGR (the bytes are reversed). So the first byte in a standard (24-bit) color image will be an 8-bit Blue component, the second byte will be Green, and the third byte will be Red. The fourth, fifth, and sixth bytes would then be the second pixel (Blue, then Green, then Red), and so on.

The image below is the resulting image from the above process.

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...

### Reference

1. [RGB Color Model](https://en.wikipedia.org/wiki/RGB_color_model)