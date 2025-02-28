# Autoencoders Exploration Notebook

## Overview
This Jupyter notebook explores three types of autoencoders (Vanilla, Denoising, Masked) using synthetic and MNIST datasets. It includes implementations, training workflows, and performance evaluations using linear probe accuracy. Key experiments investigate how bottleneck dimensions affect reconstruction error and feature quality.

## Features
- **Autoencoder Architectures**:
  - Vanilla Autoencoder
  - Denoising Autoencoder (with Gaussian noise)
  - Masked Autoencoder (with feature dropout)
- **Datasets**:
  - Synthetic dataset with configurable high-variance dimensions
  - MNIST handwritten digits
- **Evaluation**:
  - Mean Squared Error (MSE) loss
  - Linear probe classification accuracy
  - Training curve visualizations

## Code Structure
1. **Datasets**  
   - `SyntheticDataset`: Generates data with controlled covariance  
   - `MNIST`: Loads and preprocesses flattened MNIST images  

2. **Model Implementations**  
   - `Autoencoder`: Base encoder-decoder architecture  
   - `DenoisingAutoencoder`: Adds input corruption during training  
   - `MaskedAutoencoder`: Randomly masks input features  

3. **Training & Evaluation**  
   - `Experiment` class handles training loops  
   - Linear probe classifier for downstream task evaluation  

4. **Experiments**  
   - Linear autoencoders with bottleneck sizes [5, 20, 100, 500]  
   - 3-repeat averaged results on synthetic data  

5. **Visualization**  
   - Reconstruction loss vs epochs  
   - Linear probe accuracy vs epochs
6. **MNIST**:
   - Runing the same experiments on the MNIST dataset.
   - Fine tunning of hyper-parameters. 
8. **Conclusion:**
   - A high-level  analysis of the reults.
