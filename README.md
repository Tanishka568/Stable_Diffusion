# Stable Diffusion: Text-to-Image Generation

**Practical No. 05 | Deep Learning / Generative AI**

- **Name:** Tanishka Vishnu Tapkir
- **PRN:** 202401110071

## 📌 Project Overview

This practical demonstrates text-to-image generation using a pretrained Stable Diffusion model with the Hugging Face Diffusers library. It explores how inference steps, guidance scale, prompts, negative prompts, and sampling schedulers influence generated images.

Stable Diffusion is a latent diffusion model that generates images from natural-language descriptions. Instead of performing the diffusion process directly on full-resolution images, it operates in a compressed latent space, making image generation more computationally efficient.

## 🎯 Objectives

- Understand the main components of a Stable Diffusion pipeline.
- Load and use a pretrained model with Hugging Face Diffusers.
- Generate images from text prompts.
- Study the effect of inference steps and guidance scale.
- Experiment with prompt variations and negative prompts.
- Compare different sampling schedulers.
- Observe image-generation time under different settings.

## 🧠 Stable Diffusion Pipeline

The pipeline consists of the following major components:

| Component | Description |
|---|---|
| Text Encoder | Converts the input prompt into text embeddings. |
| U-Net | Predicts and removes noise from the latent representation. |
| Scheduler | Controls the denoising process and updates the latent values. |
| Variational Autoencoder (VAE) | Decodes the final latent representation into an image. |

## 🧪 Experiments

### 1. Text-to-Image Generation

Generate images using original prompts, such as:

- A botanical research station
- An underwater library
- A miniature railway station inside a tree

### 2. Effect of Inference Steps

Compare image generation using the following inference steps:

`[5, 10, 20, 35]`

The experiment uses a fixed prompt and seed to help observe how the number of denoising steps affects the generated image and execution time.

### 3. Effect of Guidance Scale

Compare guidance scale values:

`[1, 4, 7.5, 11, 15]`

Guidance scale controls how strongly the generated image follows the input prompt.

### 4. Prompt Variations

Generate images from different descriptions and observe how changes in wording influence the output.

### 5. Negative Prompt Experiment

Compare image generation with and without a negative prompt. Negative prompts specify visual characteristics that should be avoided.

### 6. Scheduler Comparison

Compare the following schedulers:

- PNDM
- DDIM
- Euler
- Euler Ancestral
- DPM-Solver

The notebook records generation time and displays the resulting images for visual comparison.

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- PyTorch
- Hugging Face Diffusers
- Transformers
- Matplotlib

## 💻 Hardware Requirements

Image generation can be computationally intensive.

- **Recommended:** NVIDIA GPU with CUDA support.
- **CPU:** May work, but generation can be significantly slower.
- **Memory:** Requirements depend on the model, device, and precision used.

The notebook selects a suitable data type based on the available device. Model download and generation time depend on the environment and network connection.

## 📊 Results and Observations

The notebook displays generated images and elapsed time for the experiments.

The observations focus on:

- How inference steps affect denoising and generation time.
- How guidance scale affects prompt adherence and image appearance.
- How prompt wording changes generated content.
- How negative prompts influence unwanted visual features.
- How different schedulers affect generation behavior and speed.

Actual results may vary depending on the hardware, model version, random seed, and library versions.

## ▶️ Running the Notebook

The main practical notebook is:

`Stable_Diffusion_Practical_05_.ipynb`

It contains the implementation, experiment comparisons, image displays, and observations. Open it in Jupyter Notebook or Google Colab and run the cells in order.

## 📚 References

- [Stable Diffusion — Hugging Face Diffusers Documentation](https://huggingface.co/docs/diffusers)
- [Hugging Face Diffusers GitHub Repository](https://github.com/huggingface/diffusers)
- [Stable Diffusion Model — Segmind Tiny SD](https://huggingface.co/segmind/tiny-sd)

---
