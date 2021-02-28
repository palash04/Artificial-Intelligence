# Sign Language Detection
This project is a part of my individual projects.

#### -- Project Status: [Completed]

## Project Objective
The purpose of this project is to detect American Sign Language (ASL) from a given image containing human hand gesture displaying one of the character from A to Z, excluding J and Z, since J and Z involves hand motion. 

### Methods Used
* Deep Learning
* Data Augmentation
* Loss Function: Cross Entropy Loss

### Technologies
* Python
* Pytorch
* Numpy, Pandas
* Jupyter
* CNN
* Image Classification

## Project Description
The project aims to achieve sign language detection from images. The project will help to enhance communication between normal people and deaf/mute people. The project is accomplished using state-of-the-art Deep Learning CNN models. The accuracy obtained on the testing dataset was 86.04%.

## Dataset Description
The dataset was acquired frorm kaggle.
Dataset contains 
1. Trainging and Testing images.
2. CSV file containing image_name and corresponding label.

## Steps involved to classify a hand gesture
1. Downloading dataset: [Link to download dataset](https://www.kaggle.com/datamunge/sign-language-mnist?select=amer_sign3.png)
2. Dataset visualization: Visualizing one image from the training dataset. </br>
![Screenshot 2021-02-28 at 19 57 23](https://user-images.githubusercontent.com/26361028/109421875-2dfb5700-79ff-11eb-96d5-fa6cab4bcfe4.png)
3. Preparing custom dataset ready to feed into our CNN architecture.
4. Creating CNN architecture.
5. Training and testing our model.

## Output of the test dataset </br>
![Screenshot 2021-02-28 at 19 58 22](https://user-images.githubusercontent.com/26361028/109421910-508d7000-79ff-11eb-9736-664dd8de627d.png)

## Results
|Hyperparameters     |  Test Dataset Accuracy   | 
|---------|-----------------|
| EPOCHS=5; LEARNING_RATE=0.001; OPTIMIZER=Adam | 61.46% |
| EPOCHS=20; LEARNING_RATE=0.001; OPTIMIZER=Adam | 77.50% |
| EPOCHS=50; LEARNING_RATE=0.001; OPTIMIZER=Adam | 86.04% |

* With further hyperparameter tuning, more than 90% test accuracy can be achieved.
