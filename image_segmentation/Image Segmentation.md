# Image Segmentation

Image segmentation is the process of dividing an image into segments or unique areas of interest.

Image segmentation is done in two main ways.

1. by connecting a series of detected edges 
2. by grouping an image into separate regions by area or distinct traits.

## Image Contours

Edge detection algorithms are often used to detect the boundaries of objects.

But, after performing edge detection you'll often be left with sets of edges that highlight not only object boundaries but also interesting features and lines.

<img src='images/edge_detected_image.png'/>

To do image segmentation, we want only complete closed boundaries that marked distinct areas and objects in an image. One technique that's useful for this is called, **Image Contouring**.

* Image contours are **continuous curves** that follow the edges along a perceived boundary.

* Contours can be used for image segmentation and they can also provide a lot of information about the shape of an object boundary.

* In OpenCV contours are best detected when there's a white object against a black background.

So before we can identify contours in an image, we will first need to create a binary threshold of image
that has black and white pixels that distinguish different objects in an image. We will then use the edges of these objects to form contours.

This binary image is often produced by a simple threshold as shown here, or by a Canny edge detector.
