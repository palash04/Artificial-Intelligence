# Facial Keypoints Detection
This project is a part of my individual projects.

#### -- Project Status: [Completed]

## Project Objective
The purpose of this project is to identify/locate 68 unique keypoints located on the face which can then be used to analyze persons emotions. The goal of identifying keypoints is achieved using the state-of-the-art Deep CNN models.

### Methods Used
* Deep Learning
* Feature Visualization
* Data Augmentation
* Loss Function: MSE Loss


### Technologies
* Python
* Pytorch
* Numpy
* Jupyter
* CNN
* Regression

## Project Description
Generally manual detection of human face expressions or emotions from an image with lots of faces is quite a cumbersome task. We want to identify face emotions to further analyze the behavior of that particular individual. So we give our task to machines which can easily do what we want. Thus we built a state-of-the-art Deep Learning CNN model which can easily detect facial keypoints. 

## Dataset Description
The dataset was acquired frorm udacity's aws cloud server. 
Dataset contains 
1. Trainging and Testing images.
2. Training and Testing csv files having keypoints associated with each images.

## Setps involved to detect keypoints
1. Downloading dataset: [Link to download dataset](https://s3.amazonaws.com/video.udacity-data.com/topher/2018/May/5aea1b91_train-test-data/train-test-data.zip)
2. Dataset visualization: Visualizing one image from the training dataset 
![Screenshot 2021-02-28 at 18 35 44](https://user-images.githubusercontent.com/26361028/109419497-c5f34380-79f3-11eb-8bf6-d0ce2b45199c.png)
3. Preparing custom dataset ready to feed into our CNN architecture.
4. Creating CNN architecture.
5. Training and testing our model.

## Output of the test dataset
![Screenshot 2021-02-28 at 19 20 23](https://user-images.githubusercontent.com/26361028/109420734-0229a280-79fa-11eb-9b59-eb23c2327348.png)
* Green color corresponds to true keypoints
* Magenta color corresponds to predicted keypoints

## Results
|Hyperparameters     |  Train_Loss   | Test_Loss |
|---------|-----------------|------|
| EPOCHS=10; LEARNING_RATE=0.01; OPTIMIZER=Adam | 0.099 | 0.077 |
| EPOCHS=10; LEARNING_RATE=0.001; OPTIMIZER=Adam | 0.476 | 0.463 |
