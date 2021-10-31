# Color-Chain
A C++ program that implements a color image processing chain converting raw image data captured by a CMOS image sensor into true color RGB images. The chain consists of 2 components: Color Interpolation and Color Correction.
Test Images: test1.bmp and test2.bmp - contain the 640x480 resolution raw images (Bayer Pattern Color Filter Array data) directly captured by a CMOS image sensor. (There are only 2 images in this project)

## Color Interpolation

Implementation of bilinear color interpolation algorithm to produce an RGB image with the same width and height as the input raw image. Boundary conditions needed to be taken into account, as pixels around the image boundary may not have neighboring pixels on one or two sides. 

## Color Correction

Following color correction matix was used:

```
[R'; G'; B'] = [1.18, -.05, -.13; -.24, 1.29, -.05; -.18, -.44, 1.62] * [R; G; B]
```

Output of Matrix multiplication was checked so that it output values <0 or >255. 

## Requirements
* C++ compiler I used Visual Studio 2010 x86
* OpenCV
