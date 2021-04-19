# HOG: Pre-processing, magniture and orientation calculation

Histogram of oriented gradients (HOG) are popular feature descriptors made hugely popular when used for pedestrian detection in 2005 [1]. These feature descriptors are obtained as the output of an intricate computational pipeline and implemented in this project. All steps until the "Linear SVM" phase of the method are manually implemented (see Figure below from [1]).

[1] Dalal N, Triggs B. Histograms of oriented gradients for human detection. In 2005 IEEE computer society conference on computer vision and pattern recognition (CVPR'05). 2005 Jun 20 (Vol. 1, pp. 886-893). IEEE.

![image](https://user-images.githubusercontent.com/76612427/115185708-3e41c100-a095-11eb-8b25-7d524f4a8952.png)

Given an input image, it is turned to greyscale and normalized to 0-1 range.

![image](https://user-images.githubusercontent.com/76612427/115185730-4ac61980-a095-11eb-8941-f338fe73793d.png)

Magnitude of gradient image is calculated with ![image](https://user-images.githubusercontent.com/76612427/115185803-6fba8c80-a095-11eb-936e-bfce2f45dc8f.png)


![image](https://user-images.githubusercontent.com/76612427/115185752-5580ae80-a095-11eb-8066-ef62d10b2371.png)

