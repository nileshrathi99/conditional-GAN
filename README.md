# Missing Value Imputation Using Conditional GAN

## Problem Description

This project aims to address missing value imputation using a Conditional Generative Adversarial Network (GAN). The task involves predicting the surrounding pixels of a known center patch in MNIST images. The initial attempt faced challenges as the generator neglected the conditioning vector. A regularization technique was introduced to improve the generator's performance.

## Instructions

1. **Data Preparation:**
   - Use a batch of MNIST images.
   - Extract 10 × 10 center patches and flatten them, forming a 100-dimensional conditioning vector.
   - Append the conditioning vector to randomly generated 100-dimensional vectors from a standard normal distribution.

2. **Training:**
   - Train the generator to synthesize MNIST-looking digits.
   - Prepare another set of real examples for comparison.
   - Train the discriminator using the combined set of real and generated examples.

3. **Regularization:**
   - Add a mean squared error term to the generator loss, penalizing the difference between the conditioning vector and the center patch of the generated image.

4. **Parameter Tuning:**
   - Investigate different λ values for the regularization term.
   - Evaluate the sensitivity of the generator to λ.

## Results

![image](https://github.com/nileshrathi99/conditional-GAN/assets/32071800/fd8c5860-eae3-4f5d-adbd-680ee930ed90)

