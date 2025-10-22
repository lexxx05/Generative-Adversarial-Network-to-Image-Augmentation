# Generative Adversarial Network for Image Dataset Augmentation

## Project Description
This project applies Generative Adversarial Networks (GANs) to augment limited image datasets. The GAN consists of a generator and discriminator trained adversarially to produce realistic synthetic images, improving data diversity for future model training.

---

## Objective
- Implement and train a GAN model to generate new synthetic images.  
- Perform architecture and hyperparameter tuning to stabilize training.  
- Evaluate model performance using the Fréchet Inception Distance (FID) metric.  
- Compare generated images from different GAN configurations.

---

## Dataset Information
- Dataset consists of real images used as references for GAN training.  
- All images are resized and normalized for consistent input.  
- The dataset is re-imported and preprocessed due to separate notebook structure.

---

## Methodology

### 1. Preprocessing
- Loaded and normalized the image dataset.  
- Resized all images to match the input shape required by the GAN architecture.

### 2. Model Development
**Base Architecture:**
- Developed a **Generator** model to create synthetic images from random noise.  
- Developed a **Discriminator** model to distinguish between real and fake images.  
- Combined both into a unified **GAN** model for adversarial training.

### 3. Model Modifications
**Version 1:**  
- Learning Rate: Discriminator 0.0001, Generator 0.0002  
- Goal: Achieve smoother and more stable training convergence.  

**Version 2:**  
- Learning Rate: Discriminator 0.001, Generator 0.002  
- Added Batch Normalization layers for training stability.  
- Goal: Improve generation quality and reduce training instability.

### 4. Evaluation
- Evaluated models using **Fréchet Inception Distance (FID)** score.  
- The second model achieved an FID of **338.76**, indicating high dissimilarity between generated and real images.  
- Visual comparisons were used to assess convergence and detect mode collapse.

---

## Results and Findings
- The first modified model produced low-quality images with faint patterns but showed partial learning.  
- The second modified model suffered from mode collapse, generating noisy and unrealistic images.  
- Training instability was the main challenge due to limited tuning time and computational constraints.

---

## Conclusion
This project explores GANs as a method for augmenting image datasets. Despite limited success in generating realistic images, it highlights key challenges such as unstable training, sensitivity to hyperparameters, and mode collapse. Further improvements could involve advanced architectures, regularization, and longer training time.
