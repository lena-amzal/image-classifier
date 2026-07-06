# CIFAR-10 Image Classifier (CNN)

## Description
This project implements a Convolutional Neural Network (CNN) to classify images from the CIFAR-10 dataset. Several model variants are trained and compared, including techniques to reduce overfitting such as Dropout and Data Augmentation.

## Dataset
CIFAR-10 is a dataset of 50,000 32x32 color training images and 10,000 test images, labeled over 10 categories:

| Class | Label |
|-------|-------|
| Airplane | 0 |
| Automobile | 1 |
| Bird | 2 |
| Cat | 3 |
| Deer | 4 |
| Dog | 5 |
| Frog | 6 |
| Horse | 7 |
| Ship | 8 |
| Truck | 9 |

## Approach
1. Data preparation
   - Normalization of pixel values (0-1)
   - One-hot encoding of labels

2. Base CNN model
   - 2 Conv2D + MaxPooling blocks (32 and 64 filters)
   - Flatten + Dense fully-connected layer
   - Trained for 20 epochs, shows overfitting starting around epoch 9

3. Overfitting reduction techniques
   - Dropout: added after each convolutional block and the dense layer
   - Data Augmentation: rotation, width/height shift, and horizontal flip applied to training images

4. Analysis and comparison
   - Training/validation loss and accuracy curves plotted for each model variant
   - Models and training histories saved for later comparison

## Technologies used
- Python
- TensorFlow / Keras
- NumPy
- Matplotlib

## Project structure
image-classifier-cnn/
├── ProjetIA.ipynb     (main notebook)
└── README.md          (this file)


## Results
The base CNN model starts overfitting after epoch 9 (validation loss increases while training loss keeps decreasing). Dropout and Data Augmentation are used to reduce this overfitting and improve generalization on the test set.
