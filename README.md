# Dog Breed CNN
**Author:** Richo Labuschagne

A Convolutional Neural Network (CNN) developed to classify images of dogs into their respective breeds.

## Overview

This project explores the use of deep learning and computer vision for automated dog breed classification. A Convolutional Neural Network is trained on a dataset of dog images and evaluated based on its ability to correctly identify different dog breeds.

The project covers the complete machine learning workflow, including:

Data preparation and preprocessing
Exploratory data analysis
Image augmentation
CNN model development
Model training
Model evaluation
Testing on unseen images



## Dataset
- Expected directory structure (PyTorch `ImageFolder` format), organized by breed:
  ```
  Dog Breed Classification/
  ├── train/
  │   ├── breed_1/
  │   ├── breed_2/
  │   └── ...
  └── test/
      ├── breed_1/
      ├── breed_2/
      └── ...
  ```
- Class names are inferred automatically from the subfolder names (sorted alphabetically by `ImageFolder`)
- **Preprocessing:**
  - Resize to 224×224
  - Convert to tensor
  - Normalize with ImageNet mean/std: `mean=(0.485, 0.456, 0.406)`, `std=(0.229, 0.224, 0.225)`
- **Batch size:** 10

> **Note:** The dataset itself is not included in this repo. Download a dog breed image dataset (e.g. from [Kaggle](https://www.kaggle.com/datasets/kabilan03/dogbreedclassification?resource=download)) and arrange it into the `train/` and `test/` folder structure above before running the notebook.
## Run Locally

Clone the project

```bash
  git clone https://github.com/Richo-Lab/CNN-dog-breed-classifier
```

Go to the project directory

```bash
  cd my-project
```

Install dependencies

```bash
  pip install -r requirements.txt
```
Run the project

```bash
  run the jupyter notebook Dog-Classification-ML.ipynb
```
```bash
  Or make use of the pre trained model dog_breed_resnet50.pth
```


## Notebook Structure

| Section | Description |
|---|---|
| Basic Imports | PyTorch, torchvision, matplotlib, numpy |
| Preparing Dataset | Image transforms (resize, tensor, normalize) |
| Loading Data | `ImageFolder` datasets and `DataLoader`s for train/test |
| Inspecting Data Shape | Visualizes a sample batch and prints tensor shapes |
| Defining the CNN Architecture | Loads ResNet-50, freezes backbone, replaces the classifier head |
| Training Loop | Trains the classifier head for 3 epochs |
| Testing Model | Evaluates accuracy and loss on the test set |
| Saving | Saves model weights to `dog_breed_resnet50.pth` |
