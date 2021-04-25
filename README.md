# Face-recognition-project-based-on-Python
#From theory to practice

1.Brightness and contrast conversion
In general, an image processing operator is a function that takes one or more images as input data and produces an output image.
# Image transformation can be divided into two types:
# 1) Point operator: Based on pixel transformation, in this kind of image transformation, the corresponding output pixel value is calculated only based on the input pixel value (sometimes with some additional information).
# 2) Neighborhood operator: Transform based on image region.
# Two commonly used operators are to multiply or add the pixel value of a point with a constant, which can be expressed as:
# g (I, j) = alpha * f (I, j) + beta, among them, the neutral position as (I, j), alpha represents the gain, beta represents the offset.The image brightness and contrast transformation is a kind of point operator, these two parameters can control the contrast and brightness respectively
#note: image pixel value range [0,255]

