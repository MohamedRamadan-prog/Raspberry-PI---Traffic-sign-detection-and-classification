# Raspberry-PI---Traffic-sign-detection-and-classification
- When we try to implement traffic sign classifier algorithm on Raspberry pi 3B+ the real-time performance was unacceptable as the value of the raspberry pi's floating point is from 900 MHZ to 1200 MHZ which is very low relative to traffic sign classifier's floating point. - So instead of convolution neural network, we worked on another solution which is template matching algorithm. - Template matching is a technique for searching and finding location of an image that are similar to a patch (template) in large image (input image).
# Notes:

- We detected and classified only 3 traffic signs to decrease processing headache on
raspberry pi, so we could achieve an acceptable real- time performance.
- We converted the input images and template images to grey scale as the inputs of
“cv2.matchedTemplate " function have to be grayscale images.
- The threshold depends on the accuracy with which we want to detect the template in the input image.
- After trial-and-error attempts, we found the threshold value that gives the best accuracy is equal to 0.6.

# Output Results
- When we applied 640 x 480 resolution, our raspberry pi's performance was 10 seconds
delay than the real-time (0.1 frame per second), so we decreased the resolution to
250 x 250 that improves our performance to 0.2 second delay ( 5 frame per second ).

![image](https://user-images.githubusercontent.com/53750465/62669125-be41f900-b98e-11e9-9e24-3013087c8327.png)


![image](https://user-images.githubusercontent.com/53750465/62669132-c306ad00-b98e-11e9-8842-1c9c1974a33a.png)


![image](https://user-images.githubusercontent.com/53750465/62669161-e7628980-b98e-11e9-80be-ee1bc79c20ca.png)
