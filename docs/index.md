# navigating-ml

My notes on navigating Machine Learning and Deep Learning.  Note, there are many paths, but these helped me get started.

## Working with Images:  A CNTK Image Tutorial Path

**Some Python required**

Below are links to Jupyter notebooks from the CNTK Tutorials along with accompanying videos by Microsoft around the MNIST digit classification example.


| Topic | Tutorial on Jupyter | Video Link |
|:------|:------|:------|
| Loading MNIST data | [Notebook 103A on CNTK GitHub](https://github.com/Microsoft/CNTK/blob/master/Tutorials/CNTK_103A_MNIST_DataLoader.ipynb) | [Video](https://www.youtube.com/watch?v=V3bT7lvm_EQ) |
| Reading MNIST data in CNTK | [Notebook 103B on CNTK GitHub](https://github.com/Microsoft/CNTK/blob/master/Tutorials/CNTK_103B_MNIST_LogisticRegression.ipynb) | [Video](https://www.youtube.com/watch?v=RbJh94AhHgw) |
| Creating and training a logistic regression classifier | [Notebook 103B on CNTK GitHub](https://github.com/Microsoft/CNTK/blob/master/Tutorials/CNTK_103B_MNIST_LogisticRegression.ipynb) | [Video](https://www.youtube.com/watch?v=9hfsVAXe2fY) |
| Predicting on data | [Notebook 103B on CNTK GitHub](https://github.com/Microsoft/CNTK/blob/master/Tutorials/CNTK_103B_MNIST_LogisticRegression.ipynb) | [Video](https://www.youtube.com/watch?v=JbhJv1OELlE) |
| Training and testing a Multilayer Perceptron | [Notebook 103C on CNTK GitHub](https://github.com/Microsoft/CNTK/blob/master/Tutorials/CNTK_103C_MNIST_MultiLayerPerceptron.ipynb) | [Video](https://www.youtube.com/watch?v=CRJZAN-fxRY) |


* Use these notebooks for free online:  [CNTK Tutorials on Azure Notebooks](https://notebooks.azure.com/cntk/libraries/tutorials)
* Use these notebooks locally (note you'll need, among other Python libraries, CNTK installed or in Docker (for macOS)):  
  1. Download the Jupyter notebook by right clicking "Raw" in the upper right-hand corner of the CNTK GitHub repo link above and "Save link as..."
  2.  On command line, navigate to the folder with the notebook, and run `jupyter notebook`, then open the notebook.


  > An aside, if you have other notebooks you'd like to include in a Docker workflow:  If using Docker (as on macOS and following [these](https://docs.microsoft.com/en-us/cognitive-toolkit/CNTK-Docker-Containers) instructions), make sure to mount any custom folders with your own notebooks when doing the `docker run` by add the `-v` flag during that command like in:
  
    `docker run -v /Users/micheleenharris/Documents/bin/ -d -p 8888:8888 --name cntk-jupyter-notebooks -t microsoft/cntk:2.0-cpu-python3.5`
## Additional Places to Go

### Getting Started Blog Articles I Love

Clearly stated and illustrated traditional machine learning, deep learning, and statistics crash course from ML @ Berkeley:
[course found here](https://ml.berkeley.edu/blog/tutorials/)

The most basic deep learning network.  A network of one neuron by the author of [Python Machine Learning](https://www.amazon.com/Python-Machine-Learning-Sebastian-Raschka/dp/1783555130/ref=sr_1_1?ie=UTF8&qid=1503038626&sr=8-1&keywords=python+machine+learning) (Sebastian Raschka):  [blog post here](https://sebastianraschka.com/Articles/2015_singlelayer_neurons.html)

The 5 Questions Data Science Can Answer by Brandon Rohrer on his excellent blog:  [blog post here](https://brohrer.github.io/five_questions_data_science_answers.html)

### Deep Learning Videos I Love

#### Just Starting Out

Melanie Warrick's [Neural Networks for Newbies](https://www.youtube.com/watch?v=g-BJSl4zV_g)

Brandon Rohrer's YouTube [channel](https://www.youtube.com/user/BrandonRohrer/videos) with tons of deep learning shorts.

A great non-mathy series on YouTube called [Deep Learning SIMPLIFIED](https://www.youtube.com/channel/UC9OeZkIwhzfv-_Cb7fCikLQ)

#### Intermediate

A great Computer Vision course out of Stanford in 2017: [videos here](https://m.youtube.com/playlist?list=PL3FW7Lu3i5JvHM8ljYj-zLfQRF3EO8sYv)

A good tutorial by Sayan Pathak at Microsoft on the CNTK deep learning Python library [here](https://www.youtube.com/watch?v=pl-kbFJ1KzU).

### Practice Makes Better

#### Kaggle Competitions

A lot of folks have recommended [Kaggle Competitions](https://www.kaggle.com/competitions) to me as they are a great place to stretch your ML muscles and start coding on an fun and exciting challenge.  There are several "start here" problems to begin solving such as [predicting survival on the Titanic](https://www.kaggle.com/c/titanic).

If you're more advanced there's a nice Computer Vision masking challenge [here](https://www.kaggle.com/c/carvana-image-masking-challenge) which closes in September 2017, but the code and data will still be up to check out.

**Thanks for Reading and Give me a Shout on Twitter if You'd Like to Chat ML or Have Some Favorite Resources Yourself**

Twitter:  @rheartpython

LinkedIn:  [https://www.linkedin.com/in/micheleenharris](https://www.linkedin.com/in/micheleenharris)

Issues or PRs welcome.

More coming soon!







