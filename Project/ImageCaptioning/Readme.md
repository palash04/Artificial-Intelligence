# Image Captioning
This project is a part of my individual projects.

#### -- Project Status: [Completed]

## Project Objective
The purpose of the project is to generate captions on processing the image.

### Methods Used
* Deep Learning
* CNN + RNN

### Technologies
* Python
* Pytorch
* Numpy, Pandas
* Jupyter
* Text Generation

## Project Description
The project aims to generate text on processing the given image. Project is buit using state-of-the-art CNN and RNN deep learning models. 

## Dataset Description
The dataset was acquired frorm kaggle.
Dataset contains 
1. Images Directory containing images
2. Captions.txt file containing image_id and corresponding caption.

## Steps involved to generate captions
1. Downloading dataset: [Link to download dataset](https://www.kaggle.com/dataset/e1cd22253a9b23b073794872bf565648ddbe4f17e7fa9e74766ad3707141adeb)
2. Dataset visualization: Visualizing an image with its caption from the dataset. </br>
![Screenshot 2021-02-28 at 20 43 32](https://user-images.githubusercontent.com/26361028/109423489-9fd69f00-7a05-11eb-8f60-ccee92f16447.png)
3. Preparing custom dataset ready to feed into our CNN architecture.
4. Creating CNN + RNN architectures. Giving the output of CNN to RNN, to generate captions.
5. Training and testing our model.

## Output of the test dataset </br>
![Screenshot 2021-02-28 at 20 45 22](https://user-images.githubusercontent.com/26361028/109423552-e1674a00-7a05-11eb-8eff-6ae293a6585c.png)
![Screenshot 2021-02-28 at 20 45 31](https://user-images.githubusercontent.com/26361028/109423555-e6c49480-7a05-11eb-8b11-9971ceeaeb2d.png)

* SOS and EOS are the start of string and end of string labels.
*  The model can be trained further to get better captions.
