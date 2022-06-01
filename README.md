# wildfire-cnn
 
## About:
This project trains a binary classification model to detect wildfires from images using Python's computer vision library Keras. Two models are trained using a convolutional neural network (CNN), one with data augmentation and one without. Data is preprocessed by applying center cropping to 200 x 200 pixels.

### Dataset
The dataset is obtained from [Kaggle](https://www.kaggle.com/datasets/phylake1337/fire-dataset?resource=download). It contains two classes, fire (755 images) and non_fire (244 images). The dataset is split into a training, validation, and testing set using a 80:10:10 split.

### Getting Started:
1. Clone this repository:  
`git clone git@github.com:ishuagrawal/wildfire-cnn.git`
2. Change directory to the repo: `cd wildfire-cnn`
3. Create a new Python 3.7 Anaconda environment.
4. Install the following packages:
    * pandas
    * tensorflow
    * pillow
    * jupyter
    * split-folders
    * scikit-learn
    * keras
    * matplotlib

### Usage:
1. Run all cells in `resize.ipynb` to standardize image size to 200 x 200 pixels and generate the `data/processed` directory. This will also split the dataset into a train, validation, and testing set under `data/output`.
2. Run all cells in `model.ipynb` (the first model). The difference is that the second model augments the training data by applying numerous variations in brightness, zooms, shifts, flips, and rotations to the images. This expands the size of the training dataset and can reduce overfitting.
3. Run all cells in `augmented_model.ipynb` (the second model). Unlike the first model, this model augments the training data by applying numerous variations in brightness, zooms, shifts, flips, and rotations to the images. This expands the size of the training dataset and can reduce overfitting.
4. Each model may take between 10-15 minutes to train on 15 epochs, which can be lowered in `hyperparameters.py` to reduce the training time.