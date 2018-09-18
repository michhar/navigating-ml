# Natural Language Processing (NLP) Resources

This is a set of materials to learn and practice NLP.  This list may also be used as general reference to go back to for a refresher.

## Courses and Course Materials (Start Here)

1.  Recurrent Neural Networks by Andrew Ng [Course Youtube Material](https://www.youtube.com/playlist?list=PLBAGcD3siRDittPwQDGIIAWkjz-RucAc7) -- **Highly recommended to start here if you've never done NLP**
2.  Stanford Deep Learning for NLP (cs224n) [Course Material](http://web.stanford.edu/class/cs224n/syllabus.html)

## Tutorials

| Topic | Title/Description | Link |
|:------|:------|:------|
| Topic Modeling | Topic modeling from Gensim official Docs | [Tutorial](https://radimrehurek.com/gensim/tutorial.html) |
| Topic Modeling and Clustering | A topic identification and document clustering algorithm tutorial with Gensim/NLTK from PyCon | [Video](https://www.youtube.com/watch?v=itKNpCPHq3I) |
| Intent and Entity Recognition | Language Understanding with Recurrent Networks from CNTK official Docs | [Tutorial](https://cntk.ai/pythondocs/CNTK_202_Language_Understanding.html) |
| Word2Vec | Vector Representations of Words from TensorFlow official Docs | [Tutorial](https://www.tensorflow.org/tutorials/word2vec) |
| Text categorization | Analysing a collection of text documents from Scikit-Learn official Docs | [Tutorial](http://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html) |
| Sequence to Sequence | A tutorial on how to summarize text and generate features using deep learning with Keras and TensorFlow | [Tutorial](https://hackernoon.com/how-to-create-data-products-that-are-magical-using-sequence-to-sequence-models-703f86a231f8) |

## Examples - Try Me!

1.  Document clustering with k-means official `scikit-learn` [Example](http://scikit-learn.org/stable/auto_examples/text/document_clustering.html#sphx-glr-auto-examples-text-document-clustering-py)
2.  Featurize free-form text data using `mmlspark` on top of primitives in SparkML via a single transformer in this official `mmlspark` [Notebook](https://github.com/Azure/mmlspark/blob/master/notebooks/samples/201%20-%20Amazon%20Book%20Reviews%20-%20TextFeaturizer.ipynb)
3.  Sequence Classification with CNTK [Example](https://github.com/Microsoft/CNTK/blob/v2.3/Examples/SequenceClassification/SimpleExample/Python/SequenceClassification.py)
4.  Sequence2Sequence with CNTK [Example](https://github.com/Microsoft/CNTK/blob/v2.3/Examples/SequenceToSequence/CMUDict/Python/Sequence2Sequence.py)

## NLP-Specific Packages

1.  `gensim`:  topic modelling [Docs](https://radimrehurek.com/gensim/) - good for word2vec, semantic similarity, LDA, LSA, etc.
2.  `nltk`:  Natural Language Toolkit [Docs](http://www.nltk.org/) - good for tokenization, stemming, tagging, parsing, corpora, etc.
3. `spacy`:  Efficient and Backed by ANNs NLP Toolkit [Docs](https://spacy.io/usage/) - good for parsing, tagging, entity recognition, text categorization, phrase matching, etc.
4.  `allennlp`:  Deep Learning for NLP from AllenNLP built on PyTorch [Ref](https://allennlp.org) - good for conditional random field, encoders/decoders, reading comprehension, semantic role, etc.

## Blog Articles

| Topic | Title/Description | Link |
|:------|:------|:------|
| Basics | 7 types of Artificial Neural Networks for Natural Language Processing | [Link](https://medium.com/@datamonsters/artificial-neural-networks-for-natural-language-processing-part-1-64ca9ebfa3b2) |
| TF/IDF | Calculating TF/IDF on How I met your mother transcripts (with `scikit-learn`) | [Link](http://www.markhneedham.com/blog/2015/02/15/pythonscikit-learn-calculating-tfidf-on-how-i-met-your-mother-transcripts/) |
| General/Sentiment Analysis | Breakthrough Research Papers and Models for Sentiment Analysis | [Link](https://blog.paralleldots.com/data-science/breakthrough-research-papers-and-models-for-sentiment-analysis/) |
|  |  | [Link]() |

## Papers

| Topic | Title/Description | Author(s) | Link |
|:------|:------|:------|:------|
| Text Classification | Fine-tuned Language Models for Text Classification (with Transfer Learning) | Jeremy Howard, Sebastian Ruder | [Link](https://arxiv.org/abs/1801.06146) |

## NLP at Scale

1.  Document classification with `pyspark` with HDInsight on Azure [Doc](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-apache-spark-ipython-notebook-machine-learning)


## Kaggle

1.  Toxic Comment Classification Challenge [Competition](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge)

## Books

TBD

## Exercises - Try Me!

| Topic | Title/Description | Link |
|:------|:------|:------|
| Sentiment Analysis | Build a sentiment analysis / polarity model `scikit-learn` | [Exercise](http://scikit-learn.org/stable/tutorial/text_analytics/working_with_text_data.html#exercise-2-sentiment-analysis-on-movie-reviews) and [Code to start](https://github.com/scikit-learn/scikit-learn/blob/master/doc/tutorial/text_analytics/skeletons/exercise_02_sentiment.py) |


List updated 2017-01-26
