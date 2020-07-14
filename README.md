# Data Scientist Nanodegree

## Capstone Project DogBreedClassifier

Ashraf Ibrahim 
14.07.2020

# Project Overview

This analysis creates a CNN which can be used as a web app or mobile app to classify images of dogs in real time and provide an estimate of the dog breed. 
If there is a human on the photo, a statement is made about which dog breed it resembles.
A detailed discussion of my approach can be found on Medium: 
https://medium.com/@ashraf.menteribrahim/dog-or-human-that-is-the-question-cb14191d95e7

# Motivation

My motivation in this project is to gain experience in setting up CNN's. I also find it exciting to work with the idea of transfer learning and to understand how to build on already trained models. 

# Problem Statement 

The main aim of this project is to set up a classifier which is able to recognize by means of dog pictures which breed this dog belongs to. This is done with the help of a Convolutional Neural Network. 




# Instructions to run the Project

To use the notebook, you must follow some steps: 

1. clone this repository 
2. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). Unzip it and place it in the repo, at location `path/to/dog-project/dogImages`.
3.  Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).  Unzip it and place it in the repo at location `path/to/dog-project/lfw.
4. Download the [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz). Place it in the repo, at location `path/to/dog-project/bottleneck_features`.
5. Download the [Inception bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogInceptionV3Data.npz). Place it in the repo `path/to/dog-project/bottleneck_features`.


## Requierements

+ Scikit-learn  
+ Numpy 
+ Pandas 
+ random
+ glob
+ keras 
+ cv2
+ matplotlib 
+ tqdm
+ PIL
+ InceptionV3


