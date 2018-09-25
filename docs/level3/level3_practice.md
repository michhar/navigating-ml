# Level 3 Challenge

In this advanced Challenge, the instructions will be a little more vague and you'll need to go figure find out much on your own, part of the learning and challenge.

> This problem set is adapted from a Custom ML Resources document written by a colleague.

_Why do this task_:  Usually, beginner tutorials around ML and neural networks begin with classifying hand-written digits from the MNIST dataset or CIFAR-10.  We are going to begin with something more challenging and much of it will be dealing with data and data formats.  This is to simulate how life will likely be in real life and it's hoped you will learn how to create machine learning models more effectively and quickly in the real world. The reason to work through the following is:

  * It will force you to read and learn from scratch.  You will learn the different label file formats, deserializers and how things compute. 
  * For for example, in energy/manufacturing you will get .png or .jpg or .tiff files and not stuff already in the perfect format. 
  * Learning this will hopefully help you understand the concept of “Data Packing”. 
  * This is not the simplest way, but it forces greater learning.

## Working with PyTorch (locally or on a DSVM/VM)

1. Image Classification

    1. Start with the Hymenoptera insect raw data
        1. Get Data from here: [click to download](https://download.pytorch.org/tutorial/hymenoptera_data.zip)
        2. Use transforms modules and other libraries to:
            * Try out some data augmentation - (random vertical flip and blur the images)
        3. Make sure you also create an example for [inference](https://en.wikipedia.org/wiki/Statistical_inference).
        2. Use Scikit-learns’s confusion matrix and classification_report to generate metrics.
            1. [Scikit-learn's confusion matrix](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html)
            2. [Scikit-learn's classification report](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html)

## Want More?

4. Do the same exact exercise with CoCo: http://cocodataset.org/#home
    1. Why do you think you get bad results?
5. Use the Out of Box Faster-RCNN solution

## TensorFlow

Train a CNN on the CIFAR-10 dataset as in this [Tutorial](https://www.tensorflow.org/tutorials/deep_cnn).

## Key Learnings

## Additional Help

* PyTorch forums - [Ref](https://discuss.pytorch.org/)
* StackOverflow with `pytorch` or `tensorflow` tag
* If using CNTK, you may send your questions to cntkhelp@microsoft.com
