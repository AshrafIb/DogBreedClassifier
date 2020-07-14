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

The main aim of this project is to set up a classifier which is able to recognize by means of dog pictures which breed this dog belongs to. This is done with the help of a Convolutional Neural Network. If a human is visible in the picture, this should be recognized and CNN should also provide an estimate of what breed of dog this human resembles. 
If there is no dog or human in the image, CNN should be able to detect this and indicate that it can only process images of dogs or humans. 

# Metrics

During the training the categorical crossentropy was used as a loss-function. This metric is suitable to be used as loss-function, if a multi-class classification is available.
More can be read here: https://machinelearningmastery.com/cross-entropy-for-machine-learning/ .
The final performance of the model was evaluated with the metric of accuracy. Unless unbalanced data is provided, this is a satisfactory metric. This metric reflects the proportion of correctly estimated cases based on all cases. In this case the accuracy score reflects the percentage of correctly classified dog breeds.

# Analysis 

This analysis follows the proposed structure of Udacity and is based on the proposed template. For this analysis, a dog image data set was used, which contains a total of 8351 images, covering 133 dog breeds. The split into training, test and validation data divides this data set as follows: 6680 training data, 835 validation data and 836 test data. 
Furthermore, several new pictures are used as criteria for the external validation. These images are located in the image folder of the repository. 

This analysis also considers several pre-trained models, including a human-face-detector, a dog-detector and image recognition algorithms like the InceptionV3. 

# Methodology 

## Preprocessing 

Firstly, pre-processing consists of rescaling incoming images to the format 224*224 pixels. Then, each image is converted into a 4D tensor and normalized by dividing each pixel by 255. 

## Implementation 

The first CNN, without transfer-learning, consisted of 14 layers in total, the architecture is well visible, and went through 20 epochs. Herewith an accuracy of 9.9282% was achieved. 
The second model is based on a pre-trained model, specifically the VGG-16, and achieved an accuracy of 38.2775% with 20 epochs. This is a considerable improvement over the first model, but still not satisfactory, as it means that in 60% of cases, images are incorrectly classified. 
In the last model transfer-learning is used again, in this case based on an InceptionV3. This is enhanced by a GlobalAveragePooling2D and a dropout layer and achieves an accuracy of 81.10% in 20 epochs, which is a significant improvement.


## Refinement 

With the InceptionV3 we experimented with further layers and epochs. Concerning the epochs it was found that from epoch 16 on a slight stagnation of the accuracy occurs, which is why the number of epochs was kept at 20. 
The addition of further dense layers has worsened the final accuracy, so that the above mentioned structure was retained. 

# Results 

As described above, the InceptionV3 with another Global Average Pooling layer and a dropout layer achieves an accuracy of 81% in the estimation of test data. 
The additional images I added were also correctly estimated, with two exceptions. These two exceptions are a picture shot from a difficult perspective and a picture showing Chewy (a real stress test for the algorithm).
Accordingly, the InceptionV3 performs significantly better than expected. This Resulst exceeds the given benchmark of 60%. 

# Further improvements 

The model usually passed my tests - only one dog breed was misclassified because the photo was taken from a difficult perspective and Chewy was classified as a dog (this was of course a difficult test). To optimize the model I would continue to do the following: 
- Perform another augmentation with more distortions. 
- Adding dog images from difficult perspectives to the data basis (diagonally above, diagonally below etc.)
- An intensive hyperparameter tuning and experimenting with the learning rate, momentum and decay (e.g. gridsearch)
- The testing of various pre-trained models!


# Instuctions to run this Notebook 

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

Copyrights:
License is given in Repository. For usage guidelines, please refer to https://www.udacity.com/legal
