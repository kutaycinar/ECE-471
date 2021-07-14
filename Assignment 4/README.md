# Dataloading: Downloading and preparing the MNIST dataset

MNIST (using Pytorch functions) is downloaded and created into indices to divide it into training, validation and testing sets. These indices will drive the creation of dataloaders aiming to facilitate the access to batches of these three subsets.

```
mnist_train = datasets.MNIST('', train=True, download=True, transform=transforms.Compose([transforms.ToTensor()]))
mnist_test = datasets.MNIST('', train=False, download=True, transform=transforms.Compose([transforms.ToTensor()])) 
```

![image](https://user-images.githubusercontent.com/76612427/115478521-31d77880-a1fb-11eb-9c20-2d73c1ec16c1.png)

# Convolutional Neural Network Creation

A small Convolutional Neural Network (CNN) is created to perform an image classification task on the handwritten digits dataset. This network is specified by defining its architecture and forward passes (the backward pass, where backpropagation happens, is automatically implemented by torch.autograd).

```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1            [16, 6, 26, 26]              60
            Conv2d-2           [16, 12, 11, 11]             660
            Linear-3                  [16, 140]          42,140
            Linear-4                   [16, 80]          11,280
            Linear-5                   [16, 40]           3,240
            Linear-6                   [16, 10]             410
================================================================
Total params: 57,790
Trainable params: 57,790
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.05
Forward/backward pass size (MB): 0.71
Params size (MB): 0.22
Estimated Total Size (MB): 0.97
----------------------------------------------------------------
```
# Calculating Losses (Mannualy and Automatically)

Loss functions are able to calculate how close to a given ground truth value a set of predictions are. The losses calculated serve as the basis for backpropagation methods.

A function is created to manually calculate the cross-entropy loss of a set of predictions and compare it with that calculated by Pytorch. SVM Multiclass loss is also calculated for illustration purposes.

```
Manual cross-entropy loss: 2.2924874871969223
Reference cross-entropy loss: 2.292487621307373
Multiclass SVM Loss: 0.8851147294044495
```

# Training CNN

Together with the creation of a network, the training routine represents the most important aspect of a DL-based image classification framework.

A training loop is implemented that predicts scores from batches of samples from the training set, and based on the losses (and gradients) calculated, updates the values of the network's parameters.

```
Updated the best model!
Epoch 0, Iteration 500 statistics:
Train acc: 98.32499999999999
Train loss:0.05424044396380486
Val acc:98.11666666666666

Updated the best model!
Epoch 0, Iteration 1000 statistics:
Train acc: 98.14375
Train loss:0.06054592075969413
Val acc:98.63333333333333

Updated the best model!
Epoch 0, Iteration 1500 statistics:
Train acc: 98.25
Train loss:0.05707443550353613
Val acc:98.72777777777777

Updated the best model!
Epoch 1, Iteration 500 statistics:
Train acc: 98.775
Train loss:0.038261727324221284
Val acc:98.97222222222221

Updated the best model!
Epoch 1, Iteration 2000 statistics:
Train acc: 98.69687499999999
Train loss:0.04269653760575966
Val acc:99.07222222222222

Updated the best model!
Epoch 2, Iteration 500 statistics:
Train acc: 99.0625
Train loss:0.029681325748853852
Val acc:99.12777777777778

End of the training loop!
```

# Testing and Displaying the Detection Results

The last segment involves the calculation of the performance of the trained model. In order to qualitatively evaluate the model, a function is created that receives a batch of samples, predicts their classes and displays the images, labels and predictions.

```
Testing accuracy: 0.985
```
![image](https://user-images.githubusercontent.com/76612427/115478975-33ee0700-a1fc-11eb-8d20-2bded06b2a84.png)
![image](https://user-images.githubusercontent.com/76612427/115478980-35b7ca80-a1fc-11eb-96e7-86f170a9f6d3.png)
![image](https://user-images.githubusercontent.com/76612427/115478707-8e3a9800-a1fb-11eb-9f8e-5270052bde7d.png)
![image](https://user-images.githubusercontent.com/76612427/115478985-38b2bb00-a1fc-11eb-9389-868c5e193290.png)
![image](https://user-images.githubusercontent.com/76612427/115478989-3c464200-a1fc-11eb-8772-6cca4082aa7f.png)

