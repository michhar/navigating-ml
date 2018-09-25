# Level 2 Preparation

Now it's time to really learn about PyTorch and classifiers such as logistic regression, multilayer perceptron, and convolutional network (CNN/ConvNet) classifiers.  The MNIST hand-written digits dataset is used in the following course to classify grey-scale images of digits.  We'll use this code in our Challenge section so go ahead and get familiar with it now by taking this course.

1. Learn concepts around neural networks for image applications and be able to answer these questions.
    1.  List the differences between a Convolutional (ConvNet/CNN) and regular Dense Neural Network (e.g Multilayer Perceptron) - two good resources:  [MLP](https://towardsdatascience.com/multi-layer-neural-networks-with-sigmoid-function-deep-learning-for-rookies-2-bf464f09eb7f) and [Convolutions - what are they](http://colah.github.io/posts/2014-07-Understanding-Convolutions/) and [CNNs](http://colah.github.io/posts/2014-07-Conv-Nets-Modular/)
    2.  List and give examples of the tunable hyperparameters one can find in a ConvNet.

2.  Gain familiarity with PyTorch
    1.  PyTorch tensor vs. numpy array (see the PyTorch [Docs](https://pytorch.org/tutorials/beginner/pytorch_with_examples.html))
    2.  Transfer Learning with a CNN (how it often happens as CNNs can be big and take time and power to train from scratch)
      Understand what is going on in this code snippet (from [Docs](https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html))
      ```pythonn
      model_ft = models.resnet18(pretrained=True)
      num_ftrs = model_ft.fc.in_features
      model_ft.fc = nn.Linear(num_ftrs, 2)
      ```