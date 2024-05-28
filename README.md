# Album Cover Image Classifier

<p align="center">
  <img width="284" alt="image" src="https://github.com/pandrum/album-cover-image-classifier/assets/38797025/052d7dc2-8a47-4c2a-bbc9-e286936fe526">
  <img width="284" alt="image" src="https://github.com/pandrum/album-cover-image-classifier/assets/38797025/0e98854a-3a29-4ac1-934c-aa04ba877751">
  <img width="284" alt="image" src="https://github.com/pandrum/album-cover-image-classifier/assets/38797025/53af9171-ab8a-4809-b7c5-3c8e81665896">
</p>

This repository contains a project for classifying album cover images using deep learning. Two models are being used, ResNet and EfficientNet. Both machine learning files are identical except for the model configuration. The model import is different, and image rescaling is omitted in the EfficientNet file. 

The models are built using TensorFlow and Keras. Both models are leveraging pre-trained weights on the ImageNet dataset. 

The dataset is split into a 70% training, 15% validation, and 15% test set. Split is done with [split-folders](https://pypi.org/project/split-folders/).

Hyperparameter tuning is performed using RandomSearch with Keras Tuner.

## Requirments
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
Ensure your dataset is organized in the following directory structure. This can be achieved with the [split-folders](https://pypi.org/project/split-folders/) tool:
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
