# Level 2 Challenge

In this intermediate Challenge, you'll apply what you've learned in the edX Deep Learning Explained course, leveraging the Jupyter notebooks you became familiar with in the course.  You'll start exploring the CIFAR-10 dataset along with other datsets in PyTorch and TensorFlow.

## Adapt Deep Learning Code

### Image Classification

Instructions to practice image classification with PyTorch

1. Get the CIFAR-10 dataset
    - Run the download script: 
2. Now let's begin working with some code.  Log into the Jupyter
  - In a code cell `! git clone ___`
  - Open this notebook:
  - Modify the notebook to work with the CIFAR-10
    * Remember you're working with RGB images instead of grayscale
  - What is the resulting average test error?  Why is this value so different from the MNIST result?  What hyperparameters can you modify to fix this?

#### Extra Credit

1. Go online and find 5 png's of cats and dogs.  Reshape them and pad them to be 32x32 pixels using the Python Pillow library (see [ImageOps](http://pillow.readthedocs.io/en/3.1.x/reference/ImageOps.html)). Test the network with these, following the guidelines and lessons you learned thus far.  Now find an image of a coconut or lime and test the network with this.  What is wrong with using a food image?
2. Create a new label called "food" and add this [fruit dataset](http://www.vicos.si/Downloads/FIDS30), leaving some out of training for testing.  Try your coconut image again.  What if now you tested with a hot dog image?

## Transfer Learning with PyTorch

Here, for ease of use and speed we'll use Transfer Learning as well.

1. ___


## TensorFlow

Easy:  Run this TensorFlow script to classify a new image (this uses a pretrained Inception V3 model):

* [https://www.tensorflow.org/tutorials/image_recognition](https://www.tensorflow.org/tutorials/image_recognition)

Intermediate: Perform this TensorFlow CNN Tutorial from Google:

* [https://www.tensorflow.org/tutorials/deep_cnn](https://www.tensorflow.org/tutorials/deep_cnn)

Advanced:  Modify this MNIST CNN TensorFlow tutorial for use with the CIFAR-10 dataset:

* [http://adventuresinmachinelearning.com/convolutional-neural-networks-tutorial-tensorflow/](http://adventuresinmachinelearning.com/convolutional-neural-networks-tutorial-tensorflow/)

## Want More?

Check out Rodrigo Benenson's [blog](http://rodrigob.github.io/are_we_there_yet/build/classification_datasets_results.html#43494641522d3130) to find out the best algorithm for classifying with CIFAR-10 and implement it.  May the force be with you.

## Additional Help

* PyTorch forums - [Ref](https://discuss.pytorch.org/)
* StackOverflow with `pytorch` or `tensorflow` tag
* If using CNTK, you may send your questions to cntkhelp@microsoft.com
