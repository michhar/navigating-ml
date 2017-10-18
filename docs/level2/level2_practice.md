# Level 2 Challenge

In this intermediate Challenge, you'll apply what you've learned in the edX Deep Learning Explained course, leveraging the Jupyter notebooks you became familiar with in the course.  You'll start exploring the CIFAR-10 dataset along with other datsets in CNTK and TensorFlow.

## Adapt Deep Learning Explained CNTK Notebooks

Here you'll adapt the Jupyter notebooks from the edX course - using the DLVM as the notebook server.  If you have a GPU at home, you may go ahead and use it, just be sure to follow the install instructions for CNTK in the [Advanced section](../adv/adv_setup/).

1. Log into the Jupyter server on the DLVM - from any browser.
2. Take the CNN Lab notebooks from edX course and use [CIFAR 10 dataset in CNTK format](https://github.com/Microsoft/CNTK/tree/master/Examples/Image/DataSets/CIFAR-10) instead to classify images into the 10 classes:  airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck instead of handwritten digits.
    1.  If you haven't cloned it yet, go ahead and clone the [CNTK GitHub repo](https://github.com/Microsoft/CNTK).
    2. Get the data by running the `install_cifar10.py` in the `CNTK/Examples/Image/DataSets/CIFAR-10/` folder of the [CNTK GitHub repo](https://github.com/Microsoft/CNTK) - it's suggested to copy this folder out to some other place to keep your CNTK repo download clean.  _Note_: this download may take several minutes.
    ...
3. Go online and find 5 png's of cats and dogs.  Reshape them and pad them to be 32x32 pixels using Pillow (see ImageOps).  Convert them to the proper CNTK format.  Test the network with these, following the guidelines and lessons you learned in the edX course.  Now find an image of a coconut or lime and test the network with this.  What is wrong with using a food image?
4. Create a new label called "food" and add this [fruit dataset](http://www.vicos.si/Downloads/FIDS30), leaving some out of training for testing.  Try your coconut image again.  What if now you tested with a hot dog image?

## Taste of TensorFlow

...

## Want More?

Check out Rodrigo Benenson's [blog](http://rodrigob.github.io/are_we_there_yet/build/classification_datasets_results.html#43494641522d3130) to find out the best algorithm for classifying with CIFAR-10 and implement it.  May the force be with you.

