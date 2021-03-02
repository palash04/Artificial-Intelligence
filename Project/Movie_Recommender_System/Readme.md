# Movie Recommender System
This project is a part of my individual projects.

#### -- Project Status: [Completed]

## Project Objective
The purpose of this project is to make a movie recommender system which would recommend a movie to the user on seeing his/her likes or ratings for several other movies. The project is built using state-of-the-art deep learning models. 

### Methods Used
* Deep Learning
* AutoEncoders
* Loss Function: MSE Loss
* Optimier: RMSProp

### Technologies
* Python
* Pytorch
* Numpy, Pandas
* Jupyter

## Project Description
The project aims to achieve optimal encoding to encode features from the movie ratings from each users. So when we have to predict ratings for the movies for which user has not seen we make use of encoding layer to decode the predictions. The Neural Network architecture is composed of stacked autoencoders which is based on state-of-the-art deep learning model.


## Dataset Description
Dataset contains 
* Movies database containing movie_id, movie_name, movie_genre
* Train and Test dataset contains user ratings for `m` total movies from movies database


## Steps involved
1. Downloading dataset: [Link to download dataset](https://grouplens.org/datasets/movielens/)
2. Preparing custom dataset ready to feed into our stacked autoencoder architecture.
4. Creating Stacked AutoEncoder (SAE) architecture.
5. Training and testing our model.


## Results
|Hyperparameters     |  Train_Loss   | Test_Loss|
|---------|-----------------| -------|
| EPOCHS=200; LEARNING_RATE=0.01; OPTIMIZER=RMSProp | 0.917 | 0.960 | 
