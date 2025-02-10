# Face Generation Using Diffusion Model

## 📋 Description

This project implements a diffusion model to generate realistic human faces by combining features from different ethnic groups (Oriental, Indian, and European). The implementation is done in PyTorch using a Jupyter notebook environment.

## 👤 Project Details
* 👨‍💻 **Author:** Rohit Kumar Manne
* 📅 **Date:** December 2024
* 🛠️ **Framework:** PyTorch
* 💻 **Environment:** Google Colab / Jupyter Notebook

## ⭐ Key Features
* 🎨 Generates realistic human faces using diffusion models
* 🔄 Blends facial features from different ethnic groups
* 📊 Uses the FairFace dataset for diverse facial images
* 🎯 Implements classifier-free guidance for better control
* 🏗️ Custom UNet architecture with time embeddings

## 🚀 Setup and Installation

### 1. Clone the Repository
```bash
git clone https://github.com/rohitkumarmanne-442/face-generation-diffusion.git
cd face-generation-diffusion
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Dataset Structure
```
Dataset/
├── european/
├── indian/
└── orientals/
```

## 💻 Implementation Details

### 📚 Components

#### 1. Dataset Class (FaceDataset)
* 📥 Handles loading and preprocessing of facial images
* 🏷️ Supports three ethnic groups with label encoding
* 🔄 Includes data transformations and augmentation

#### 2. Model Architecture (UNet)
* ⏱️ Incorporates time embeddings for diffusion process
* 🎛️ Includes label conditioning for ethnic control
* 🔗 Features skip connections and up/down sampling paths

#### 3. Diffusion Process
* 📊 Manages noise schedule and sampling procedure
* 🎯 Implements classifier-free guidance
* 🎨 Controls image generation process

#### 4. Training Pipeline
* 🔄 250 epochs training configuration
* ⚙️ Adam optimizer with learning rate 1e-4
* 📈 Progress tracking and checkpoint saving

## 📝 Usage

### 1. Open Jupyter Notebook
```bash
jupyter notebook Face_Generation_Diffusion.ipynb
```

### 2. Update Dataset Paths
```python
european_path = "path/to/european"
indian_path = "path/to/indian"
oriental_path = "path/to/orientals"
```

### 3. Run Notebook
* ▶️ Run all cells sequentially

## 🎯 Results

The model generates:
* 👤 Pure ethnic facial features
* 🔄 Two-way combinations:
  * 🔹 Oriental-Indian
  * 🔹 Oriental-European
  * 🔹 Indian-European
* 🔀 Three-way ethnic combinations

## 📦 Dependencies
```
torch >= 1.7.0
torchvision
numpy
Pillow
tqdm
matplotlib
IPython
jupyter
```

## 📚 Citation
```bibtex
@misc{manne2024face,
  author = {Manne, Rohit Kumar},
  title = {Face Generation Using Diffusion Model},
  year = {2024},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/rohitkumarmanne-442/face-generation-diffusion}}
}
```

## 📄 License
This project is licensed under the MIT License.

## 🙏 Acknowledgments
* 🏢 FairFace dataset creators for providing diverse facial images
* 🛠️ PyTorch community for the deep learning framework
* 🔬 Diffusion Models research community

## 📧 Contact
For questions or feedback, please open an issue in the repository.
