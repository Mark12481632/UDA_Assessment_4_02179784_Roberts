# UDA_Assessment_4_02179784_Roberts
# Author: Mark D. Roberts (CID 02179784)

Project Overview:
=================
    The objective of this project is to create a simple framework to test how well image classification model(s) perform when
    presented with corrupted images. The idea is that different classification models can be swapped-in/out and tested with
    minimal changes.
    Also, the type of image corruption/degradation - e.g. faded or noisy images - can be easily changed.
    In this particular implementation of the framework:
        * we use a model that has been pre-trained to classify non-corrupted images with an accurancy of over 97%.
            This model was created using the guidance provided in chapter 8 of [1], and is based on refining an
            already pretrained model.
            The "refining" of the model has been omitted here as it took several hours to build this model and the full
            dataset needed exceeded the 100MB data limit.
        * all images used in the refining and testing of this model are cat and dog images taken from the Kaggle website: 
          "Cat and Dog Images" - the link is in the associated PDF for this assessment.
        * testing will be performed using two types of image degradation:
            1. uniform random noise, but this could be easily replaced by other noise patterns (e.g. Gaussian) if desired and
            2. image fading, which is simulated by colour strength reduction.

    The testing image dataset consists of 2000 images - 1000 cat and 1000 dog images.

General Information:
====================
    * This script was run on a Macbook Pro. with 16 GB of RAM, 3.1 GHz Quad-Core Intel Core i7.
    * The total run time of the Jupyter notebook was (approx) 2 hours.
    * The Github repository for all code and datasets can be obtained by cloning the repository:
           https://github.com/Mark12481632/UDA_Assessment_4_02179784_Roberts.git
    * The model used to classify the images is built on TensorFlow and Keras (versions are in the PDF for this assessment).
    * Altered images need to be saved to disk - so write permission for the notebook is required!!

The Jupyter notebook has 4 cells which are used in the assessment PDF.  Starting at CELL-2 the python libraries are loaded.
From this reference the following cells create the results used in the assessment PDF:
   - Cell 8 : The images of the cats with noise added (Fig. 1)
   - Cell 9 : The graph showing Model accuracy for noisy images (Fig. 2)
   - Cell 12: The images of cats that have been faded (Fig. 3)
   - Cell 13: The graph showing Model accuracy for faded images (Fig. 4)


References:
===========
[1] - Deep Learning with Python (Francios Chollet, Manning Publications, ISBN-13: 978-1617296864)
