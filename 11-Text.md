
# 11-Text

* Structuring and cleaning text data
* EDA using term frequency (Jane Austen novels)
* Text classification (Naive Bayes with newsgroup documents)
* Unsupervised topic modeling (LSA & LDA newsgroups, IMDb reviews)

## Notebooks

* [10-learning-faces-exercises](https://colab.research.google.com/drive/1SiToIlQDKaSEqOqT1Brb4SvtBv00x3Y0)
* [10-learning-faces-exercises2](https://colab.research.google.com/drive/1Wy3-EAJSp6PAr5pEt98F6GHGkgjoncQ2)
* [11-austen-nlp-exercises](https://colab.research.google.com/drive/15zGJswgIkO5Ih4on4_L0wM9yLp2TOqKn)
* [scratch-notebook](https://colab.research.google.com/drive/1H4sj-XdST_PqBXQTrkutsamSFrOs2wNG)
* [poll everywhere](https://pollev.com/pbogden) 

## Videos & Reading (after Thanksgiving)

* I'll be assigning some videos
* ISLR2 -- Chapter 10
  * Read this if you find it interesting, but not if it seems too complex.

## PCA (review)

* PCA -- SVD -- dimensionality reduction, unsupervised learning, and (to a lesser extent, as we'll see) clustering
* VanderPlas -- In Depth: PCA (p431)
* [05.09-Principal-Component-Analysis.ipynb](https://github.com/jakevdp/PythonDataScienceHandbook/blob/master/notebooks/05.09-Principal-Component-Analysis.ipynb)
  * We've seen PCA for dimensionality reduction with linear models in high dimensions.
  * We'll see it act as a clustering method with text (e.g., LSA with the 20 NewsGroups)
  * Performs fairly well as a clustering method when the features are uncorrelated

## learning-faces

* exercises

## text mining

* [Text mining with R](https://www.tidytextmining.com/index.html) 
  * A good book with a lot of good material. It doesn't touch neural networks.
  * The book's hard to read if you don't know R.
* [NLTK book](https://www.nltk.org/book/)
  * A good book focussed on the NLTK toolkit by leaders in that community. It doesn't touch neural networks.
  * It's in Python. It's old (published in 2009) and it won't be updated.
  * [Natural Language Pocessing with Python](https://learning.oreilly.com/library/view/natural-language-processing/9780596803346/) (2009) available from O'Reilly.
* [Natural Language Processing with Transformers](https://learning.oreilly.com/library/view/natural-language-processing/9781098136789)
  * A very new book about the latest technologies: attention/transformers in deep learning (neural networks).
  * It's in Python and assumes a knowledge of neural networks (Tensorflow, Pytorch).
  * It's brand new (published June 2022). We'll look at neural networks later on.

## Historical context

* 50's hype (the cold war)
  * the promise of machine translation -- Chomsky (linguist)
  * the birth of AI -- Rosenblatt's perceptron
  * Figure credits: Raschka [ch02.ipynb](https://github.com/rasbt/python-machine-learning-book-3rd-edition/blob/master/ch02/ch02.ipynb)
<img src="https://raw.githubusercontent.com/rasbt/python-machine-learning-book-3rd-edition/master/ch02/images/02_01.png" width="500px">

<img src="https://raw.githubusercontent.com/rasbt/python-machine-learning-book-3rd-edition/master/ch02/images/02_04.png" width="500px">

* 60's failure
  * Recognition that machine requires context or it makes mistakes
    * For example: "the spirit is willing but the flesh is weak." 
    * Translated back and forth with Russian, became: "the vodka is good but the meat is rotten."
* 70's winter
  * Federal funding dries up
* 80's hype
  * expert systems (knowledge base & rules) -- business applications
  * mainframes (DEC and Sun)
  * the rise of the IBM PC (and the first version of Apple)
* 90's winter
  * crash of expert systems -- mainframes replaced by desktops
  * birth of the web and open source
  * the era of statistical NLP and text corpora
* 00's spring
  * growth of the web
  * development of ML & statistical algorithms
  * hardware (Moores law) and big data
* 10's progress
  * rediscovery of backpropagation
  * computational power with GPUs
  * deep neural networks and novel applications
* 20's hype?
  * transformers, attention -- deep networks mimic cognitive attention and provide context (as opposed to bag of words)
  * pre-trained systems
  * big labeled datasets
* Is another winter coming...?
* References
  * [AI Winter](https://en.wikipedia.org/wiki/AI_winter)
  * [Natural Language Processing](https://en.wikipedia.org/wiki/Natural_language_processing)

## austen
