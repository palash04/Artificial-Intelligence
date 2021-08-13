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

- **Generator**
  - I had used a `U-Net` ([arXiv:1505.04597](https://arxiv.org/abs/1505.04597)) like architecture for the generator, which is simply an encoder-decoder architecture with skip connections in between them.

![U-Net](https://user-images.githubusercontent.com/26361028/129304211-82ba1f2f-75d4-4bf0-b421-7eb8d2a74518.png)

<p align="center">[Image Courtesy: Author's paper]</p>

  - Precisely, the encoder channels vary as  `in_channels -> 64 -> 128 -> 256 -> 512 -> 512 -> 512 -> 512` and the decoder's channel sizes vary accordingly.

- **Discriminator**
  - For the discriminator, a `PatchGAN` is used. A `PatchGAN` is similar to a common discriminator, except that it tries to classify each patch of N × N size whether it is real or fake.
  - In our case, we take N = 70. This is in our code achieved by using a Convolutional network whose receptive field is 70 on the input image to the discriminator. Mathematically, this can be checked to be equivalent to what has been described in the paper.
  - The channel sizes in our `PatchGAN ` vary as `in_channels -> 64 -> 128 -> 256 -> out_channels`.

- **Encoder**
  - This is the additional architecture incorporated by me, in order to alleviate the problem of mode collapse.
  - It takes in a pair of `positive sample` and a `negative sample`, and outputs corresponding vectors of `d` dimensions each.
  - The L1 norm between vectors is maximized to achieve diverse results.
  - Here, positive sample is a pair of fake generated image `B_hat` and the latent noise `Z ~ N(0,1)` which is responsible for generating `B_hat` and, negative sample is a pair of fake generated image `B_hat` and the latent noise `Z' ~ N(0,1)` which is not responsible for generating `B_hat`


![Architecture](https://user-images.githubusercontent.com/26361028/129305392-68593736-fda8-47dc-9659-785b92c710ff.png)
<p align="center">[The above figure summarizes all three architectures used.]</p>

## Results:

![Result1](https://user-images.githubusercontent.com/26361028/129305645-e1db5304-83e7-4b93-b896-3ead15cdd464.png)
![Result2](https://user-images.githubusercontent.com/26361028/129305664-76bda638-c205-4355-b0b2-3df7b580984e.png)

## Note
Result format [Source - Generated_1 - Generated_2 - Generated_3]

## Conclusion:
As we can see from the results generated, we are indeed getting diverse results, but the percentage of diverse results is less, inorder to incorporate more diverse results, we can have `k` negative samples for every positive sample while training the GAN architecture.


## Authors:
* Palash Mahendra Kamble - [palash04](https://github.com/palash04/)

## Acknowledgements
* I would like to thank the authors of the paper for the public dataset found [here](http://efrosgans.eecs.berkeley.edu/pix2pix/datasets/)
