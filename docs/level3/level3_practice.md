# Level 3 Challenge

In this advanced Challenge, the instructions will be a little more vague and you'll need to go figure find out much on your own, part of the learning and challenge.

> This problem set is adapted from a Custom ML Resources document written by a colleague.

_Why do this task_:  Usually, beginner tutorials around ML and neural networks begin with classifying hand-written digits from the MNIST dataset.  We are going to begin with something more challenging and much of it will be dealing with data and data formats.  This is to simulate how life will likely be in real life and it's hoped you will learn how to create machine learning models more effectively and quickly in the real world. The reason to work through the following is:

  * It will force you to read and learn from scratch.  You will learn the different label file formats, deserializers and how things compute. 
  * For energy/manufacturing you will get .png or .jpg or .tiff files and not stuff already in the perfect format. 
  * Learning this will hopefully help you understand the concept of “Data Packing”. 
  * This is not the simplest way, but it forces greater learning.

## Working with CNTK Locally (DLVM is also OK)

**Use the CNTK Manual as reference: [CNTK Manual on GitHub](https://github.com/Microsoft/CNTK/tree/master/Manual)**

This is focusing for the Energy/Manufacturing Vertical.

1. Understand Label Files & Mini Batch Sources:
    1. CTF & Image: [http://dacrook.com/complex-neural-network-data-modelling-with-cntk/](http://dacrook.com/complex-neural-network-data-modelling-with-cntk/)
    2. Sequence: [http://dacrook.com/deep-learning-match-making-with-recurrent-networks/](http://dacrook.com/deep-learning-match-making-with-recurrent-networks/)
2. Image Classification:
    1. Start w/ CIFAR 10 for image classification using a Jupyter Notebook (use [CNTK Manual on GitHub](https://github.com/Microsoft/CNTK/tree/master/Manual))
        2. Get Data from here: [CIFAR-10 data](https://www.kaggle.com/c/cifar-10/data)
        1. Start w/ a CTF deserializer
            1. Use Image library w/ numpy and CNTK's io libraries to write a ctf file containing the data in flattened arrays
        2. Use the Image deserializer next
            1. Try out a few transforms.  You will have to read the CNTK docs pages for transforms. [CNTK transforms](https://cntk.ai/pythondocs/cntk.io.transforms.html)
        3. Make sure you also create an example for [inference](https://en.wikipedia.org/wiki/Statistical_inference).
        2. Use Scikit-learns’s confusion matrix and classification_report to generate metrics.
            1. [Scikit-learn's confusion matrix](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html)
            2. [Scikit-learn's classification report](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html)


## Azure ML Workbench

3.  Do the same thing w/ Azure ML Workbench
    1. Set up
        1. Create a workspace
	    2. Create a git repo in VSTS
	    3. Create a project linked to the repo
        2. Re-write as a single training script and execute via docker locally.
        1. Add in Azure ML Workbench’s logging apis.
        1. Try out a Convolutional Network
        2. Use the Azure ML Workbench Operationalization CLI to create a container.
            1. Create a local container
            2. Pull the local container and test locally
            3. Deploy a real time container to Azure Container Services
            4. Test against this.
            5. TIP:  You will either send the image via the body as an array of float32 or as a byte64 encoded string.

4. Do the same exact exercise with CoCo: http://cocodataset.org/#home
    1. Why do you think you get bad results?
5. Use the Out of Box Faster-RCNN solution w/ CNTK and CoCo

## Taste of TensorFlow

Train a CNN on the CIFAR-10 dataset as in this [Tutorial](https://www.tensorflow.org/tutorials/deep_cnn).

## Key Learnings

Object detection v.s. Classification, Data Prep and pipelines.

## Places to go for Help

**If you run into trouble, email CNTK Help cntkhelp@microsoft.com and also create a stack overflow with tag `cntk`, then send the link to SO to CNTK Help.  Alternatively, create an Issue on the CNTK GitHub repo.**