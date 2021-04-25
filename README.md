# Face-recognition-project-based-on-Python
#From theory to practice
#123.jpg为初始处理图片

1.Brightness and contrast conversion
In general, an image processing operator is a function that takes one or more images as input data and produces an output image.
# Image transformation can be divided into two types:
# 1) Point operator: Based on pixel transformation, in this kind of image transformation, the corresponding output pixel value is calculated only based on the input pixel value (sometimes with some additional information).
# 2) Neighborhood operator: Transform based on image region.
# Two commonly used operators are to multiply or add the pixel value of a point with a constant, which can be expressed as:
# g (I, j) = alpha * f (I, j) + beta, among them, the neutral position as (I, j), alpha represents the gain, beta represents the offset.The image brightness and contrast transformation is a kind of point operator, these two parameters can control the contrast and brightness respectively
#note: image pixel value range [0,255]

2.Noise processing
# The less noise, the better the picture quality
Image noise: that is, unnecessary or redundant information in image data
# Robustness: A system or organization has the ability to resist or overcome adverse conditions. When an algorithm model is said to be robust, it indicates that some abnormal data have little or no impact on the overall performance of the algorithm model.
# Adding appropriate amount of noise to the training data can make the trained model more robust and improve the performance of the model
#------------- Add a noise TAB
Pepper and salt noise: also known as impulse noise, is a kind of noise that is often seen in images. It is a random white or black dot, which may be black pixels in the bright area or white pixels in the dark area (or both).
Salt and pepper noise can be caused by sudden and strong interference with the image signal, analog-to-digital converter or bit transmission errors, etc.For example, a failed sensor results in a minimum pixel value, and a saturated sensor results in a maximum pixel value.
# Add salt and pepper noise to image simulation is achieved by randomly acquiring pixel points and setting them as high brightness points and low gray points
# Gaussian noise: Gaussian noise refers to a kind of noise whose high green density function obeys Gaussian distribution.In particular, if the amplitude distribution of a noise obeys the Gaussian distribution and its power spectral density is uniformly distributed, it is called the white Gaussian noise.
# The second moment of Gaussian white noise is uncorrelated, while the first moment is constant, which refers to the correlation of successive signals in time.Gaussian noise includes thermal noise and three-mile noise.
Gaussian noise is determined by its mean value of events and the two instantaneous covariance function. If the noise is stationary, the mean value is independent of time, while the covariance function becomes a correlation function only related to the difference between the two instantaneous values under consideration, which is equivalent to the power spectral density in the sense.
