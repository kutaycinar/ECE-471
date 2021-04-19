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

## HOG: 2 x 2 cell block normalization

The last step in calculating the HOG feature descriptor is to normalize blocks containing multiple cells to compensate for lighting and contrast changes. Blocks composed by 2 x 2 cells are used (i.e., 16x16 pixels for cell_size=8) with an L-2 norm normalization scheme. 






