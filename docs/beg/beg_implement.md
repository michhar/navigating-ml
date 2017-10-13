# Beginner Challenge

In this Beginner Challenge you'll learn about basic ML and neural networks hands-on with Jupyter notebooks and Python.  You'll be introduced to scikit-learn, CNTK, and TensorFlow as Python packages and the Azure ML Workbench tool.  You'll work with the fruit dataset, the sklearn images dataset and CIFAR-10 (tiny images) dataset.

## Custom Vision

1. Download the [fruit dataset](http://www.vicos.si/Downloads/FIDS30) and build a fruit image classifier with [https://customvision.ai/](https://customvision.ai/).

## Basic Neural Nets

1.  Use [Azure Notebooks](https://notebooks.azure.com) for this tutorial.  Fire up a blank Python 3.5 Jupyter notebook for this.
2. Get the following sample image dataset loaded in your Jupyter notebook: [sklearn image dataset](http://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_sample_images.html#sklearn.datasets.load_sample_images)
3. Adapt a from-scratch Perceptron as in this [Jupyter notebook](https://github.com/rasbt/python-machine-learning-book-2nd-edition/blob/master/code/ch02/ch02.ipynb) to train and test on the image dataset.
    - Use the URL option when opening up a new notebook in Azure Notebooks
    - Or, download by right clicking on "Raw" and "Save link as..."
    - Re-implement the Perceptron in scikit-learn
4. Adapt a from-scratch Multilayer Perceptron as in this [Jupyter notebook](https://github.com/rasbt/python-machine-learning-book-2nd-edition/blob/master/code/ch12/ch12.ipynb)
    - Use the URL option when opening up a new notebook in Azure Notebooks
    - Or, download by right clicking on "Raw" and "Save link as..."
    - Re-implement the MLP in scikit-learn

## Running and Testing Locally with Azure ML Workbench

- Train your MLP from scikit-learn inside of Azure ML Workbench
- Test
- Check run history for metrics
- Containerize
- Deploy
- Test the endpoint

## Transfer Learning on the Deep Learning Virtual Machine with CNTK

- Connect to your Linux Deep Learning Virtual Machine (DLVM) in Azure with x2go (see instructions [here](https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/provision-deep-learning-dsvm#how-to-access-the-deep-learning-virtual-machine)).
- Use ResNet to train a CIFAR 10 classifier
    - Download the [CIFAR 10 dataset in CNTK format](https://github.com/Microsoft/CNTK/tree/master/Examples/Image/DataSets/CIFAR-10)
    - Run this script on the command line on the DLVM, found [here](https://github.com/Microsoft/CNTK/tree/master/Examples/Image/Classification/ResNet/Python#trainresnet_cifar10py), to train your classifier with Transfer Learning (base model is ResNet).

## Taste of TensorFlow

Here, you'll take advantage of the Inception-v3 model trained on the ImageNet dataset, to simply classify a new image.

Go through up to and including "Usage with Python API" such that you can classify your own jpeg (note, there are 1000 classes in this Inception-v3 model):  [Tutorial](https://www.tensorflow.org/tutorials/image_recognition#top_of_page) using your Linux DLVM.

- "Git clone" the indicated repository
- Run the script locally on the command line
- Run the script with your own jpeg
- Take a peek at the code to see how the model was built

## Additional Help

- StackOverflow with `cntk` tag
- Issues on CNTK GitHub repo
- StackOverflow with `sklearn` tag