# Generative-Adversial-Network
Preparation of GAN using Fashion MNIST dataset

This project implements a Generative Adversarial Network (GAN) to generate handwritten digits similar to those in the MNIST dataset. The GAN consists of two neural networks, a Generator and a Discriminator, which compete against each other to improve their performance.

Architecture
Generator Network:
The generator network takes a random noise vector (often sampled from a standard normal distribution) as input and passes it through multiple layers of fully connected layers, batch normalization, and ReLU activations, followed by a final output layer with a tanh activation function that generates a 28x28 image.

Discriminator Network:
The discriminator network is a binary classifier that takes a 28x28 image as input and passes it through a series of convolutional and fully connected layers with Leaky ReLU activations, ending with a single sigmoid output that represents the probability of the image being real.

Loss Function
Generator Loss:
The generator's goal is to maximize the discriminator's error in classifying fake images as real. Thus, the generator is updated to minimize the negative log probability of the discriminator being wrong.

Discriminator Loss:
The discriminator's objective is to correctly classify real and fake images. It is updated by minimizing the cross-entropy loss between its predictions and the actual labels (real or fake).
