## Overview

This repository contains an implementation of a diffusion model for generating MNIST images. Diffusion models have gained popularity for their ability to generate high-quality images through a process of iterative refinement. This project demonstrates how such a model can be applied to the MNIST dataset for generating handwritten digits. Main implementation ideas are from the paper "Denoising Diffusion Probabilistic Models (DDPM) by Jonathan Ho et al ([link to the paper](https://arxiv.org/abs/2006.11239)).  In this paper diffision models, their training and their generation mechanism is explained from a probabilistic perspective, and their main contribution is to generate realistic images of a dataset using a diffision model to formulate and learn their distribution.   

## Features of Diffusion Models

Diffusion models are a class of generative models characterized by:

- **Iterative Refinement**: Unlike traditional generative models, diffusion models generate images through a series of steps that gradually refine a noise input into a coherent image.
- **Probabilistic Framework**: They model the data distribution using a probabilistic approach, allowing for the incorporation of complex image features.
- **High-Quality Outputs**: Capable of generating highly detailed and realistic images.
- **Stability**: Often exhibit greater training stability compared to other generative models like GANs.
- **Flexibility**: Can be adapted for various types of data, including images, audio, and more.

## About This Implementation

In this implementaion, a very simple model consisting of only linear layers andd silu activation function to predict noise in each step is used, since the dataset is fairly simple. Number of forward steps is set to 20 instead of 1000, and beta is linearly increased from 0.001 to 0.7, different from the original paper. Also in the generation process, it is posiible to neglect the addition noise used in the paper during sapling process. 

## Requirements

- Python 3.x
- PyTorch
- NumPy
- Matplotlib

## Results

Results on MNIST dataset, generating 50 images, 5 from each digit:

![MNIST results](results/results-MNIST.png)
