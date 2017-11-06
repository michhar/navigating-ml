# Level 2 Challenge

In this intermediate Challenge, you'll apply what you've learned in the edX Deep Learning Explained course, leveraging the Jupyter notebooks you became familiar with in the course.  You'll start exploring the CIFAR-10 dataset along with other datsets in CNTK and TensorFlow.

## Adapt Deep Learning Explained CNTK Notebooks

### Image Classification

Here you'll adapt the Jupyter notebooks from the edX course - using the DLVM as the notebook server.  If you have a GPU at home, you may go ahead and use it, just be sure to follow the install instructions for CNTK in the [Advanced section](../level3/level3_setup).

1. Get the CIFAR-10 dataset (in CNTK format)
  * SSH into your DLVM ([Doc](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-vm#connect-to-vm) - need to add 'azureuser' to the ssh command however!  Note, you can also use the VM through a Unix Desktop by following this [Doc](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/use-remote-desktop#install-a-desktop-environment-on-your-linux-vm))
    - `ssh azureuser@<your VMs public ip here` (e.g. `ssh azureuser@52.174.34.95`, which you can get from the Azure portal, portal.azure.com)
    - `cd` into the `notebooks` folder
    - Clone the CNTK Github repo
    - `cd CNTK/Examples/Image/DataSets/CIFAR-10/` to go to the data folder where the download script lives
    - Run the download script: `python install_cifar10.py` (this might take some time as it's creating the CNTK text files as well as image files from the original Toronto CIFAR 10 archived dataset)
2. Now let's begin working with some code.  Log into the Jupyter server on the DLVM - from any browser (note: you'll need to agree to keep going to this site despite the certificate warning - don't worry, this is normal)
  - Point your browser to `https://<VM DNS name or IP Address>:8000/`" ([Doc](https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/dsvm-ubuntu-intro#tools-installed-on-the-data-science-virtual-machine-for-linux))
  > If this notebook is not familiar to you go back to the Preparation section and watch the videos [here](level2_prep).
  - Open `CNTK_103D_MNIST_ConvolutionalNeuralNetwork.ipynb` (or better yet, open a copy you've made on the VM) - this will be the CNN notebook you modify to fit the CIFAR-10 dataset (instead of MNIST), remembering that your data is now at `../Examples/Image/DataSets/CIFAR-10/`.
  - Modify the notebook to work with the CIFAR-10
    * Remember you're working with RGB images instead of grayscale
  - What is the resulting average test error?  Why is this value so different from the MNIST result?  What hyperparameters can you modify to fix this?

#### Extra Credit

1. Go online and find 5 png's of cats and dogs.  Reshape them and pad them to be 32x32 pixels using the Python Pillow library (see [ImageOps](http://pillow.readthedocs.io/en/3.1.x/reference/ImageOps.html)).  Convert them to the proper CNTK text format.  Test the network with these, following the guidelines and lessons you learned in the edX course.  Now find an image of a coconut or lime and test the network with this.  What is wrong with using a food image?
2. Create a new label called "food" and add this [fruit dataset](http://www.vicos.si/Downloads/FIDS30), leaving some out of training for testing.  Try your coconut image again.  What if now you tested with a hot dog image?

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

Here, for ease of use and speed we'll use Transfer Learning as well.

1. Run [this](https://github.com/Microsoft/CNTK/tree/master/Examples/Image/Classification/ResNet/Python#trainresnet_cifar10py) script on the command line on your DLVM, to train your classifier with Transfer Learning (the base model here is [ResNet](https://arxiv.org/abs/1512.03385)).


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
