# HOG: Pre-processing, magniture and orientation calculation

Histogram of oriented gradients (HOG) are popular feature descriptors. These feature descriptors are obtained as the output of an intricate computational pipeline and implemented in this project. All steps until the "Linear SVM" phase of the method are manually implemented.

Given an input image, it is turned to greyscale and normalized to 0-1 range.

![image](https://user-images.githubusercontent.com/76612427/115185730-4ac61980-a095-11eb-8941-f338fe73793d.png)

Magnitude of gradient image is defined as:

![image](https://user-images.githubusercontent.com/76612427/115185803-6fba8c80-a095-11eb-936e-bfce2f45dc8f.png)

Orientation is defined as:

![image](https://user-images.githubusercontent.com/76612427/115185881-9082e200-a095-11eb-897a-aad9f0d7e88c.png)

Plotted magnitude of input image:

![image](https://user-images.githubusercontent.com/76612427/115185752-5580ae80-a095-11eb-8066-ef62d10b2371.png)

## HOG: Creation of cells and Histograms of Oriented Gradients

After computing the orientation and magnitude images (matrices) of a given grayscale input. The next step is to divide the grayscale input into 8x8 non-overlapping cells and create, for each cell, a histogram of oriented gradients. The HOG formation is illustrated in the image below (considering a small 3x3 cell):

![image](https://user-images.githubusercontent.com/76612427/115186038-d5a71400-a095-11eb-8833-248513a1ed6d.png)

## HOG: 2 x 2 cell block normalization

The last step in calculating the HOG feature descriptor is to normalize blocks containing multiple cells to compensate for lighting and contrast changes, as described by the authors: "Gradient strengths vary over a wide range owing to local variations in illumination and foreground-background contrast, so effective local contrast normalization turns out to be essential for good performance." [1]

Blocks composed by 2 x 2 cells are used (i.e., 16x16 pixels for cell_size=8) with an L-2 norm normalization scheme. 

![image](https://user-images.githubusercontent.com/76612427/115186140-0424ef00-a096-11eb-98db-2a65c9528b64.png)


# References
[1] Dalal N, Triggs B. Histograms of oriented gradients for human detection. In 2005 IEEE computer society conference on computer vision and pattern recognition (CVPR'05). 2005 Jun 20 (Vol. 1, pp. 886-893). IEEE.
[2] Mallick, Satya. "Histogram of Oriented Gradients." 2016. Available at: https://www.learnopencv.com/histogram-of-oriented-gradients/






