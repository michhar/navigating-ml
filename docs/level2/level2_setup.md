# Setup

1. (Deploy when ready if you don't have it yet) [Linux (Ubuntu) Deep Learning Virtual Machine](https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/provision-deep-learning-dsvm) Standard NC6
> Tip: place everything for this set of challenges in the same resource group to tear down together at the end.

2. Ensure Jupyter notebooks are working.
    - "access the Jupyter notebook server from any host. Just navigate in the browser to `https://<VM DNS name or IP Address>:8000/`" ([Doc](https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/dsvm-ubuntu-intro#tools-installed-on-the-data-science-virtual-machine-for-linux) - check out "Jupyter notebook" for more)
    
3.  Download Azure Machine Learning Workbench locally from this [Doc](https://docs.microsoft.com/en-us/azure/machine-learning/preview/quickstart-installation).

> Plan to work with CNTK locally?  Make sure you check out which versions of Python it works with and note it's for Windows and Ubuntu-flavored Linux as of now.  If you are on a different OS there's a Docker image that is easy to set up and begin right away with CNTK.
 
 3.  CNTK Install - [Docs](https://docs.microsoft.com/en-us/cognitive-toolkit/setup-windows-python?tabs=cntkpy22#installing-cntk-for-python-on-windows)
 
 > TensorFlow can be found on all Linux and Windows Data Science Virtual Machines and Deep Learning Virtual Machines along with a long list of common data science tools - see [Docs](https://docs.microsoft.com/en-us/azure/machine-learning/data-science-virtual-machine/overview)
