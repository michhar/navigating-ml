# Level 2 Challenge

In this intermediate Challenge, you'll apply what you've learned in the edX Deep Learning Explained course, leveraging the Jupyter notebooks you became familiar with in the course.  You'll start exploring the CIFAR-10 dataset along with other datsets in CNTK and TensorFlow.

## Adapt Deep Learning Explained CNTK Notebooks

Here you'll adapt the Jupyter notebooks from the edX course - using the DLVM as the notebook server.  If you have a GPU at home, you may go ahead and use it, just be sure to follow the install instructions for CNTK in the [Advanced section](../adv/adv_setup/).

1. Log into the Jupyter server on the DLVM - from any browser.
2. Take the CNN Lab notebooks from edX course and use [CIFAR 10 dataset in CNTK format](https://github.com/Microsoft/CNTK/tree/master/Examples/Image/DataSets/CIFAR-10) instead to classify images into the 10 classes:  airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck instead of handwritten digits.
    1.  If you haven't cloned it yet, go ahead and clone the [CNTK GitHub repo](https://github.com/Microsoft/CNTK).
    2. Get the data by running the `install_cifar10.py` in the `CNTK/Examples/Image/DataSets/CIFAR-10/` folder of the [CNTK GitHub repo](https://github.com/Microsoft/CNTK) - it's suggested to copy this folder out to some other place to keep your CNTK repo download clean.  _Note_: this download may take several minutes.
3. Go online and find 5 png's of cats and dogs.  Reshape them and pad them to be 32x32 pixels using Pillow (see ImageOps).  Convert them to the proper CNTK format.  Test the network with these, following the guidelines and lessons you learned in the edX course.  Now find an image of a coconut or lime and test the network with this.  What is wrong with using a food image?
4. Create a new label called "food" and add this [fruit dataset](http://www.vicos.si/Downloads/FIDS30), leaving some out of training for testing.  Try your coconut image again.  What if now you tested with a hot dog image?

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

Easy:  Run this TensorFlow script to classify a new image (this uses a pretrained Inception V3 model):
* [https://www.tensorflow.org/tutorials/image_recognition](https://www.tensorflow.org/tutorials/image_recognition)

Intermediate: Perform this TensorFlow CNN Tutorial from Google:
* [https://www.tensorflow.org/tutorials/deep_cnn](https://www.tensorflow.org/tutorials/deep_cnn)

Advanced:  Modify this MNIST CNN TensorFlow tutorial for use with the CIFAR-10 dataset:

* [http://adventuresinmachinelearning.com/convolutional-neural-networks-tutorial-tensorflow/](http://adventuresinmachinelearning.com/convolutional-neural-networks-tutorial-tensorflow/)

## Want More?

Check out Rodrigo Benenson's [blog](http://rodrigob.github.io/are_we_there_yet/build/classification_datasets_results.html#43494641522d3130) to find out the best algorithm for classifying with CIFAR-10 and implement it.  May the force be with you.


## Additional Help

* StackOverflow with `cntk` or `tensorflow` tag
* For CNTK specific help you may send your questions to cntkhelp@microsoft.com.
