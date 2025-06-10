# **Thermal Cat Image Generator**

This repository presents a simulation framework for generating **thermal-style images of cats** using advanced generative deep learning models. The goal is to develop a **simulated thermal camera** for animals, useful for research, training, and educational purposes—especially where access to real thermographic equipment is limited or cost-prohibitive.

---

## 📌 Project Overview

We simulate thermal images of cats using a combination of real thermographic imagery and standard RGB images from the Cats Dataset. To achieve this, we evaluate a variety of deep generative approaches:

- DCGAN  
- CycleGAN  
- StyleGAN  
- Pix2Pix  
- StyleGAN2-ADA  
- Diffusion-based models  

Additionally, we experiment with **style-mixing** between RGB and thermal latent spaces to explore hybrid generation.

---

## 🔬 Key Features

- Comparative evaluation using **FID metrics**  
- Training on RGB, thermal, and augmented datasets  
- Style-mixing experiments to transfer color distribution from thermal to RGB-based structure  
- Support for **128×128** and **256×256** image sizes  
- Detailed experiment logic and results inside `Cats.ipynb`

---

## 📊 Summary of Results

| Model                     | FID Score ↓ |
|--------------------------|-------------|
| CycleGAN                 | 350.37      |
| StyleGAN                 | 300.00      |
| Diffusion Model          | 280.00      |
| StyleGAN2-ADA            | **101.37**  |
| StyleGAN2-ADA (RGB only) | **8.12**    |

> Among all methods, StyleGAN2-ADA trained on RGB cat images produced the most thermographically plausible results.

---

## 🛠️ Usage Instructions

All model loading, training, and image generation pipelines are implemented in the Jupyter notebook `Cats.ipynb`. This notebook contains:

- Model download and initialization  
- Image preprocessing  
- Generation and style-mixing examples  
- FID calculation and result analysis  

---

## 📝 Future Work

We aim to improve thermal simulation realism by incorporating:

- **Body-region segmentation** for localized heat mapping  
- **Physiological priors**, such as known thermal patterns in animals  
- **Environmental simulation** to adapt thermal response to external conditions  

---

## 🧠 Keywords

`thermal image simulation`, `GAN`, `cats`, `infrared`, `style transfer`, `image generation`, `deep learning`, `computer vision`
