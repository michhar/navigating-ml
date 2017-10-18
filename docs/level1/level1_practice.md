# Level 1 Challenge

In this Beginner Challenge you'll learn about basic ML and neural networks hands-on with Jupyter notebooks and Python.  You'll be introduced to scikit-learn, CNTK, and TensorFlow as Python packages and the Azure ML Workbench tool.  Here and throughout these challenges you'll work with these image datasets: the fruit FIDS30 dataset, the Kaggle Fashion MNIST dataset and the CIFAR-10 (tiny images) dataset.

## Custom Vision

1. Download the [fruit dataset](http://www.vicos.si/Downloads/FIDS30) and build a fruit image classifier with [https://customvision.ai/](https://customvision.ai/).

## First Custom ML

### Image Classification

Create a Python program to classify images from Fashion MNIST Dataset (get [here](https://www.kaggle.com/zalando-research/fashionmnist/data)) leveraging code samples from the Python Data Science Handbook - [Ref](https://jakevdp.github.io/PythonDataScienceHandbook/05.02-introducing-scikit-learn.html#Application:-Exploring-Hand-written-Digits).  Do this in a Jupyter notebook (any service or locally) - recall you learned about this tool the Getting Started and Level 1 Preparation sections.  It might help to examine the existing data format for `sklearn.datasets.load_digits` so that you can convert into that format to utilize the algorithms in `sklearn` (scikit-learn).  Refer to Chapter 2 and 3 of this Handbook for information on data manipulation in Python if not already familiar.

### Object Detection

Create a Python program to detect cats in 2D images by leveraging code samples from the Python Data Science Handbook - [Ref](https://jakevdp.github.io/PythonDataScienceHandbook/05.14-image-features.html).  Do this in a Jupyter notebook (any service or locally) - recall you learned about this tool the Getting Started and Level 1 Preparation sections.  It might help to examine the existing data format for `sklearn.datasets.fetch_lfw_people` so that you can convert into that format to utilize the algorithms in `sklearn` (scikit-learn) to create this detector.  Refer to Chapter 2 and 3 of this Handbook for information on data manipulation in Python if not already familiar.


## Basic Neural Nets

The purpose of the Basic Neural Nets exercises are to familiarize you with how a simple neuron works and then set of a few neurons - all from the ground-up - this knowledge will serve you well.  It will really get to the core of neural nets and give you a perfect "from scratch" introduction (the code template already exists around the infamous iris dataset, you'll just make it work with some fashionable images).  If we want to get to know deep neural nets, why not dive in deep to start!

1.  Use [Azure Notebooks](https://notebooks.azure.com) for this tutorial.  Fire up a blank Python 3.5 Jupyter notebook for this.
2. Get the following sample image dataset loaded in your Jupyter notebook: [train and test Fashion MNIST Dataset (Source: Kaggle)](https://www.kaggle.com/zalando-research/fashionmnist/data)
3. Adapt a from-scratch Perceptron as in this [Jupyter notebook](https://github.com/rasbt/python-machine-learning-book-2nd-edition/blob/master/code/ch02/ch02.ipynb) to train and test on the image dataset.
    - Use the URL option when opening up a new notebook in Azure Notebooks
    - Or, download by right clicking on "Raw" and "Save link as..."
    - Re-implement the Perceptron with `sklearn` (scikit-learn)
4. Adapt a from-scratch Multilayer Perceptron (MLP) as in this [Jupyter notebook](https://github.com/rasbt/python-machine-learning-book-2nd-edition/blob/master/code/ch12/ch12.ipynb)
    - Use the URL option when opening up a new notebook in Azure Notebooks
    - Or, download by right clicking on "Raw" and "Save link as..."
    - Re-implement the MLP with `sklearn`

## Running and Testing Locally with Azure ML Workbench

Now that you've got a couple of implementations of a Multilayer Perceptron, go ahead and setup an experiment in Azure ML Workbench, a nice new public preview Data Science workbench, to train and test on the Fashion dataset above.

Use the iris dataset template and tutorial as an example - see the [Docs](https://docs.microsoft.com/en-us/azure/machine-learning/preview/tutorial-classifying-iris-part-1).

- Read your csv train file into Azure ML Workbench
- Modify the iris template to train a model with any of the above classification algorithms locally in docker
- Test with the `score.py` file locally in docker
- Check run history for metrics (observe the use of scikit-learn's confusion matrix, etc.)
- Containerize
- Deploy this to a Kubernetes cluster
- Test the endpoint in any script or application that you want to build (in any language)

## Transfer Learning on the Deep Learning Virtual Machine with CNTK

Now, we are going to totally switch gears and tools.  We'll spin up a Deep Learning Virtual Machine and leverage raw Python scripts already kindly prepared for us on a classic image dataset, CIFAR-10, which has ten classes.  Here, for ease of use and speed we'll use Transfer Learning as well.

- Connect to your Linux Deep Learning Virtual Machine (DLVM) in Azure with x2go (see instructions in [Docs](https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/provision-deep-learning-dsvm#how-to-access-the-deep-learning-virtual-machine)).
- Use ResNet to train a CIFAR 10 classifier
    1.  Go ahead and clone the [CNTK GitHub repo](https://github.com/Microsoft/CNTK).
    2. Get the data by running the `install_cifar10.py` in the `CNTK/Examples/Image/DataSets/CIFAR-10/` folder of the [CNTK GitHub repo](https://github.com/Microsoft/CNTK) - it's suggested to copy this folder out to some other place to keep your CNTK repo download clean.  _Note_: this download may take 10-20 minutes - it's a lot of data and data conversions.
    3. Run [this](https://github.com/Microsoft/CNTK/tree/master/Examples/Image/Classification/ResNet/Python#trainresnet_cifar10py) script on the command line on your DLVM, to train your classifier with Transfer Learning (the base model here is [ResNet](https://arxiv.org/abs/1512.03385)).

## Taste of TensorFlow

This will serve as a gentle intro to TensorFlow.  Here, you'll take advantage of the Inception-v3 model pre-trained on the ImageNet dataset and simply classify a new image using the pre-built script.

Go through up to and including "Usage with Python API" such that you can classify your own jpeg (note, there are 1000 classes in this Inception-v3 model):  [Tutorial](https://www.tensorflow.org/tutorials/image_recognition#top_of_page) using your Linux DLVM.

- "Git clone" the indicated repository
- Run the script on the command line on your DLVM
- Run the script with your own jpeg
- Take a peek at the code to see how the model was built

## Additional Help

- StackOverflow with `sklearn`, `cntk` or `tensorflow` as tag
- Issues on CNTK GitHub repo