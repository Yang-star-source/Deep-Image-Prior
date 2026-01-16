# Deep Image Prior Implementation : Denoising , Inpainting and Super Resolution

This repository contains a PyTorch implementation of **Deep Image Prior**, exploring how a neural network structure alone can act as a prior for image restoration tasks without large training datasets.

## Projects Included

This repository covers three main image restoration tasks. You can run them directly in Google Colab:

| Task | Notebook | Description | Run |
| :--- | :--- | :--- | :--- |
| **Denoising** | `Deep_Image_Prior_Denoising.ipynb` | Removes noise from corrupted images using the neural network prior. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Yang-star-source/Deep-Image-Prior/blob/master/Deep_Image_Prior_Denoising.ipynb) |
| **Inpainting** | `Deep_Image_Prior_Inpainting.ipynb` | Fills in missing or corrupted regions of an image (e.g., removing text or scratches). | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Yang-star-source/Deep-Image-Prior/blob/master/Deep_Image_Prior_Inpainting.ipynb) |
| **Super Resolution** | `Deep_Image_Prior_Super_Resolution.ipynb` | Upscales low-resolution images while preserving details. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Yang-star-source/Deep-Image-Prior/blob/master/Deep_Image_Prior_Super_Resolution.ipynb) |

## How to Run (Reproducibility)

These notebooks are optimized for **Google Colab**. 

1. Click the **"Open in Colab"** badge above for the task you want to test.
2. In Colab, go to **Runtime > Change runtime type** and select **GPU** (T4 GPU is sufficient).
3. Run all cells (`Ctrl + F9`) for inpainting and super resolution notebook.
   - The code is set up to automatically handle dependencies and image downloading.
4. For denoising notebook , check the description to choose whether a multiple times denoising is needed, manually click and run.

## Repository Structure

- `images/`: Contains sample images used for testing the model.
- `Deep_Image_Prior_*.ipynb`: The main source code for each experiment.

## Notes
- This implementation uses an untrained U-Net architecture.
- Optimization is performed on a single image at runtime (no pre-training required).
- For Denoising , specifically can only sharpen CAT images by importing Latent Diffusion I built (Unconditional Single Class Image Generation model).

## Citation

This project implements the methods proposed in **Deep Image Prior**.

```bibtex
@article{UlyanovVL17,
    author   = {Ulyanov, Dmitry and Vedaldi, Andrea and Lempitsky, Victor},
    title    = {Deep Image Prior},
    journal  = {arXiv:1711.10925},
    year     = {2017}
}
