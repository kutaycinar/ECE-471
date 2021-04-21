# Dataloading, feature extraction, model training and evaluation for image classification

After collecting and creating a 240 image dataset for three classes (boat, ship, guitar), they are shuffled and then paritioned into test, train and validation sets.

Example of shuffled test and training data:

![image](https://user-images.githubusercontent.com/76612427/115477773-87ab2100-a1f9-11eb-915c-754a12fc21ac.png)

![image](https://user-images.githubusercontent.com/76612427/115477783-8aa61180-a1f9-11eb-8982-c4a538b67b29.png)

# Feature extraction: HOG, Hue Histogram and Raw RGB

Features are extracted to drive machine lenarning-based image classifications.

# Creating and training the classifiers

In this project, there are three classifiers used to test the efficacy of the feature matrices.

- Support Vector Machine (SVM)
- Logistic Regresion (also know as maximum-entropy classification, log-linear classifier)
- Gaussian Naive Bayes

# Evaluating the classifiers

A function is created to calculate a number of metrics that will help evaluating the different pairs of classifier/features. The performance metrics this function calculates are:

- Class-specific recall
- Class-specific precision
- Average recall
- Average precision
- Average F1-Score
- Average Accuracy

![image](https://user-images.githubusercontent.com/76612427/115478211-80384780-a1fa-11eb-87ce-27306e1a5657.png) ![image](https://user-images.githubusercontent.com/76612427/115478217-83cbce80-a1fa-11eb-9220-718a5c1c4b8e.png) ![image](https://user-images.githubusercontent.com/76612427/115478222-86c6bf00-a1fa-11eb-8d9f-42ceb081fd99.png)

The average precision, average recall and F1-score metrics of each of the nine model/feature pairs are shown now in a single table. 

![image](https://user-images.githubusercontent.com/76612427/115478229-8e866380-a1fa-11eb-997e-dbdec04edf6f.png)
