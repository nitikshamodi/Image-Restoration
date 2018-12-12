# Image-Restoration

## Introduction
Image can be corrupted due to various reasons like noise, distortion, exposure, defocus blur, movement blur etc. Distortion occurs in real life while transmitting an image through a medium or while taking an image. This leads to some loss of information. Thus we want to restore the information. It seems that blurring is an irreversible operation and that the information is lost, especially in case of a big blur radius where everything the image seems to be smoothed very much. However, in most cases we know the properties of the medium from which the image is corrupted  and the image can be restored.  In this project, we consider the case of defocus blur and additive gaussian noise. 

## The Blurring process
Let f be the original image, let h be be the blurring function,  let g be the resulting blurred image and let n be the noise function. 

Then, g(x,y) = f(x,y)*h(x,y) + n(x,y)

Where * denotes convolution.
The process of applying the blur function is convolution, i.e., some path of the image convoles into a pixel of the blurred image. If no noise is added to the system then we can restore the image by simply reversing the convolution process i.e. by using deconvolution. 
In this project we use the gaussian blur function. 

## The Noise process
There can be many reasons for noise in a model such as thermal vibration, magnetic influence, temperature, etc.  Noise can be considered as a random process which is usually modelled using Gaussian additive noise. The noise is additive because it is added to noise that might be intrinsic in the system. It is defined by two parameters: mean and variance. 

## Filters used for deblurring
In this project we have used only grayscale images.  The process for colored images is the same. Each step has to be applied to the R, B and G channels separately. 

### Inverse Filter
We know that

$ g(x,y) = f(x,y)*h(x,y) + n(x,y) $





