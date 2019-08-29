<<<<<<< HEAD
# ASL Image Recognition

Image recognition on ASL signed alphabet using machine learning and computer vision techniques.

##Description

This project is an exercise in applying different methods of dimensionality reduction to image recognition in the domain of hand signed alphabet letters. The dataset is comprised of 81,000 200x200 images, 3000 unique images for each signed letter (including one with an empty background to help differentiate the background with the signer's hand) in full RGB. Instead of fitting the model directly to the dataset, we can make the processing a little less memory intensive with a some transformations.


###Installing

To set up the appropriate environment, install 'pip' to manage each package:
```bash
pip install sklearn
```
You will need the following:
* Numpy
* CSV (OpenCV)
* Pickle
* Pandas
* Sklearn
* PIL (Pillow)

###Process

** Link Image **

Our objective is to make our dataset leaner while maintaining fidelity in our model. The preprocessing steps are as follows:

1. Convert dataset to grayscale, reducing range of RGB values.
2. Normalize brightness/exposure of dataset for accuracy.
3. Extract edges from dataset to use as our primary feature.
4. Resize images down to 75x75, which would still preserve acceptable image definition.
5. Use PCA for dimensionality reduction and extract key features for our model (3000 components will account for 85% of the variance).
6. Use a SVM model (scales well to high dimensionality data) for our predictions.
7. Use grid search and cross validation (k=3) to better tune our parameters.

###Discussion

Accuracy hovers around 85-90 which is pretty good considering how similar some features are between certain letters and letters like 'i' and 'j' differ by an action that cannot be represented in an image. This example shows one misidentified case and its label.

** Link Image **

Possible future expansion of this project can include motion capture and identification in real time.

##Acknowledgments
* OpenCV's [Canny Edge Detection](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_imgproc/py_canny/py_canny.html) provided the edge detection module.
* Our dataset was taken from Akash's [ASL Alphabet](https://www.kaggle.com/grassknoted/asl-alphabet).

=======
# COGS118BASL
>>>>>>> e76014419d05e328281102e8b67bcad3c31703f0
