# Diversity in paired Image to Image Translation
This project was made as the final project for DS 265 - Deep Learning for Computer Vision course in Spring 2021 at Indian Institute of Science (IISc) Bangalore, India.

#### -- Project Timeline: [March 01, 2021 - May 30, 2021]
#### -- Project Status: [Completed]

## Abstract
Diversity in paired image-to-image translation (I2IT) aims at generating diverse output images in the target domain for a given input image. Conditional generative adversarial networks (cGANs) are often used for this particular task of modeling conditional distribution. However, cGANs are prone to ignore the latent code and learn to model unimodal distribution in conditional image-to-image translation. This problem of learning unimodal distribution is often called as mode collapse which is a typical issue of GANs. So, I approach to resolve this issue of mode collapse in image synthesis by incorporating an additional network (Encoder)in GAN architecture along with Generator and Discriminator. The encoder will discriminate between the positive samples and negative samples in order to maximize the information between two latent codes. The incorporated method achieves variations in output images for different latent code on the given input image, but fails to produce realistic looking images.

## Datasets
I had tested this project with the following dataset released public by the authors (link in [Acknowledgements](#acknowledgements) section)
- Facades


## Prerequisites
- Python 3.7.10 or above
- [PyTorch](https://pytorch.org/) 1.9.0 or above
- CUDA 10.2 (or other version corresponding to PyTorch) to utilize any compatible GPU present for faster training

### Keywords
* Generative Adversarial Networks
* Pytorch 
* Image to Image Translation
* Mode Collapse
* Jupyter Notebook

## Arhchitecture



## Results:

## Authors:
* Palash Mahendra Kamble - [palash04](https://github.com/palash04/)

## Acknowledgements
* I would like to thank the authors of the paper for the amazing public dataset found [here](http://efrosgans.eecs.berkeley.edu/pix2pix/datasets/)
