# GAN for Handwritten Digit Generation

This repository contains an implementation of a Generative Adversarial Network (GAN) using PyTorch. The model is trained to generate realistic handwritten digits similar to those in the MNIST dataset.


# Overview
Generative Adversarial Networks (GANs) are a class of machine learning frameworks designed by a pair of neural networks, the Generator and the Discriminator. These two networks are trained simultaneously through adversarial training:

* Generator: Learns to produce data that is similar to the real dataset.
* Discriminator: Learns to distinguish between real data (from the dataset) and fake data (produced by the Generator).
In this project, the GAN is trained on the MNIST dataset, which contains images of handwritten digits (0-9). The goal is to generate new, synthetic images of handwritten digits that look as if they came from the dataset.

# Model Architecture
### Generator
* The Generator takes a random noise vector (latent space of dimension 128) as input and generates a flattened image of size 28x28 (784 dimensions).
* It uses fully connected layers followed by ReLU activations and a final Sigmoid activation to output pixel values between 0 and 1.
### Discriminator
* The Discriminator is a binary classifier that receives a flattened image as input and outputs a probability indicating whether the image is real or fake.
* It uses fully connected layers followed by ReLU activations and a final Sigmoid activation to output a probability score.
### Loss Functions
* Discriminator Loss: Measures how well the Discriminator can distinguish real images from fake ones. It's a combination of losses on real and fake images.
* Generator Loss: Measures how well the Generator can fool the Discriminator into classifying its fake images as real.

# Usage
### Training
To train the GAN on the MNIST dataset:

1. Ensure the MNIST dataset is downloaded by PyTorch.
2. The model is trained for 20 epochs by default, with a batch size of 32. During training, the Discriminator and Generator are trained in alternating steps.

# Visualizing Generated Digits
During training, the script periodically visualizes a grid of images generated by the Generator from a fixed noise vector. This allows you to monitor the quality of the generated digits as training progresses.

# Results
The trained Generator should be able to produce realistic-looking handwritten digits. The quality of the generated images typically improves with more training epochs.

![image](https://github.com/user-attachments/assets/f23e1aaf-fe93-4f0f-97c5-c7bf4b91bbed)

![image](https://github.com/user-attachments/assets/1df355e5-1654-4fad-b621-0c09e91206c7)

![image](https://github.com/user-attachments/assets/458368db-b8dd-49f8-a287-a0dca99a5e00)

![image](https://github.com/user-attachments/assets/0f700304-c3fe-46be-89c7-e1470de94132)

![image](https://github.com/user-attachments/assets/eef11396-e8cb-4cfc-b1e5-32819f3276a6)






