Face Generation Using Diffusion Model
This project implements a diffusion model to generate realistic human faces by combining features from different ethnic groups (Oriental, Indian, and European). The implementation is done in PyTorch using a Jupyter notebook environment.
Overview

Author: Rohit Kumar Manne
Date: December 2024
Framework: PyTorch
Environment: Google Colab / Jupyter Notebook

Key Features

Generates realistic human faces using diffusion models
Blends facial features from different ethnic groups
Uses the FairFace dataset for diverse facial images
Implements classifier-free guidance for better control
Custom UNet architecture with time embeddings

Setup and Installation

Clone the repository:

bashCopygit clone https://github.com/rohitkumarmanne-442/face-generation-diffusion.git
cd face-generation-diffusion

Install required packages:

bashCopypip install -r requirements.txt

Dataset Structure:

CopyDataset/
├── european/
├── indian/
└── orientals/
Implementation Details
The notebook contains the following components:

Dataset Class: FaceDataset

Handles loading and preprocessing of facial images
Supports three ethnic groups with label encoding
Includes data transformations and augmentation


Model Architecture: UNet

Incorporates time embeddings for diffusion process
Includes label conditioning for ethnic control
Features skip connections and up/down sampling paths


Diffusion Process

Manages noise schedule and sampling procedure
Implements classifier-free guidance
Controls image generation process


Training Pipeline

250 epochs training configuration
Adam optimizer with learning rate 1e-4
Progress tracking and checkpoint saving



Usage

Open the Jupyter notebook:

bashCopyjupyter notebook Face_Generation_Diffusion.ipynb

Update the dataset paths in the notebook:

pythonCopyeuropean_path = "path/to/european"
indian_path = "path/to/indian"
oriental_path = "path/to/orientals"

Run all cells sequentially

Results
The model can generate:

Pure ethnic facial features
Two-way ethnic combinations:

Oriental-Indian
Oriental-European
Indian-European


Three-way ethnic combinations

Dependencies
Major dependencies include:

torch >= 1.7.0
torchvision
numpy
Pillow
tqdm
matplotlib
IPython
jupyter
