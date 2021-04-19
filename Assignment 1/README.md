# Programming: introduction to Python, Colab and OpenCV

## Basic image operations 

Using Python and OpenCV in this project, input images are loaded, transformed, displayed and saved.

Given a color RGB input image, we can extract the blue channel by setting red and green channels to all zeros:

![image](https://user-images.githubusercontent.com/76612427/115183738-47309380-a091-11eb-80ba-f0dda1a5b2a3.png)

A greyscale image can be manually optained as seen above by using ITU-R 601-2 luma transform:

```
L = R * 299/1000 + G * 587/1000 + B * 114/1000
```

![image](https://user-images.githubusercontent.com/76612427/115183932-9eceff00-a091-11eb-9fbd-8a608ec29837.png)

Images can be multiplied by a scalar to make them darker or brighter:

![image](https://user-images.githubusercontent.com/76612427/115184092-f53c3d80-a091-11eb-8392-611de7d5c6e8.png)

Applying gamma correction formula to an image:

![image](https://user-images.githubusercontent.com/76612427/115184136-0b49fe00-a092-11eb-8174-713455ef5684.png)

Histogram calculation:

![image](https://user-images.githubusercontent.com/76612427/115184205-2b79bd00-a092-11eb-8ee3-b82b007e34d1.png)

Histogram after changing contrast of an image:

![image](https://user-images.githubusercontent.com/76612427/115184366-89a6a000-a092-11eb-8d89-bceac1f64a45.png)

Given a greyscale input image and a color reference, we can match color by using histograms:

![image](https://user-images.githubusercontent.com/76612427/115184393-96c38f00-a092-11eb-80de-741e4c01fe86.png)
