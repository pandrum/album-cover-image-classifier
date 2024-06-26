# Album Cover Image Classifier

This repository contains a project for classifying album cover images using deep learning. Two models are being used, ResNet and EfficientNet. Both machine learning files are identical except for the model configuration. The model import is different, and image rescaling is omitted in the EfficientNet file. 

The models are built using TensorFlow and Keras. Both models are leveraging pre-trained weights on the ImageNet dataset. 

The data that was being used for the two machine learning models in this project can be recreated from this repository: [EquiGen Album Cover Dataset](https://github.com/pandrum/equigen/blob/main/README.md).

The dataset is split into a 70% training, 15% validation, and 15% test set. Split is done with [split-folders](https://pypi.org/project/split-folders/).

Hyperparameter tuning is performed using RandomSearch with Keras Tuner.

## Requirements
```
numpy
tensorflow
PIL
os
seaborn
scikit-learn
matplotlib
keras-tuner
```

Install the required packages using pip:
```
pip install numpy tensorflow pillow seaborn scikit-learn matplotlib keras-tuner
```

## Data Setup
Ensure your dataset of images is organized in the following directory structure. This can be achieved with the [split-folders](https://pypi.org/project/split-folders/) tool:
```
split/
  ├── train/
  │   ├── class_1/
  │   ├── class_2/
  │   └── ...
  ├── val/
  │   ├── class_1/
  │   ├── class_2/
  │   └── ...
  └── test/
      ├── class_1/
      ├── class_2/
      └── ...
```

## Training Procedure
The epoch, hyperparameter trials and hyperparameters can be tweaked freely. Callbacks are currently implemented where the model with highest validation accuracy is saved locally. History is also saved locally for plotting train and validation graphs.

## Usage
1. Clone the repository:
```
git clone https://github.com/yourusername/album-cover-classification.git
cd album-cover-classification
```
2. Install the required packages:
```
pip install -r requirements.txt
```
3. Organize your dataset as described in the Data Setup section.
4. Run the notebook to train the model and evaluate the results.

## Acknowledgements
This project uses the ResNet101 and EfficientNetVB0 architecture that are pre-trained on ImageNet, and leverages Keras Tuner for hyperparameter tuning.
