# DogBreedClassifier

This repository is for my Udacity Data Science Nanodegree Capstone project. In this project it was about setting up a CNN, which can identify dog breeds. 
A detailed discussion of my approach can be found on Medium: 
https://medium.com/@ashraf.menteribrahim/dog-or-human-that-is-the-question-cb14191d95e7

# 1 Motivation and Overview

The motivation was to create a CNN, which can classify dog breeds via images, based on the pre-trained InceptionV3 model. The underlying Dataset consists roughly of 8400 images of dogs from 133 different breeds. 

# 2 Installation 

To use the notebook, you must follow some steps: 

1. clone this repository 
2. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). Unzip it and place it in the repo, at location `path/to/dog-project/dogImages`.
3.  Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).  Unzip it and place it in the repo at location `path/to/dog-project/lfw.
4. Download the [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz). Place it in the repo, at location `path/to/dog-project/bottleneck_features`.
5. Download the [Inception bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogInceptionV3Data.npz). Place it in the repo `path/to/dog-project/bottleneck_features`.


# 3 Steps of Analysis

1. Detecting Humans (based on OpenCV's Face-     Classifier) 
2. Detecting Dogs (using ResNet-50 pretrained Model)
3. Create a CNN from Scratch 
4. Using a pre-trained CNN
5. Using another pre-trained CNN 
6. Writing my final Algorithm 
7. Testing my Model
8. Final Thoughts

## 4 Model Performance

Accuracy of final Model is about 81%. This model is based on the pre-trained InceptionV3.  

## 5 Requierements

+ Scikit-learn  
+ Numpy 
+ Pandas 
+ random
+ glob
+ keras 
+ tensorflow
+ cv2
+ matplotlib 
+ tqdm
+ PIL
+ InceptionV3


