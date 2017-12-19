# week2 Sequence Models

## Introduce to Word Embeddings
* Word Representation (v1) The problem of one hot encode is it cannot represent the similarities between different words >> learn featurized representation, word embedding ([van der Maaten & Hinton 2008](http://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf)).
* Using word embeddings (v2) To learn needs 1-100B words. Similiar with face encoding [Taigman et al. 2014](https://www.cs.toronto.edu/~ranzato/publications/taigman_cvpr14.pdf)
* Properties (v3) analogies [Mikolov et al. 2013](https://www.aclweb.org/anthology/N13-1090), cosine similarity.
* Embedding matrix (v4)  E*oj = ej
 
## Word2vec & GloVe
* Learning word embeddings (v1) [Bengio et al. 2003](http://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf)
* Word2Vec (v2) [Mikolov et al. 2013](https://www.aclweb.org/anthology/N13-1090) skip-grams idea. 

  the problem of softmax model? speed! >> hierachical softmax
 
* Negative Sampling (v3) [Mikolov et al. 2013](https://www.aclweb.org/anthology/N13-1090) 

  How to define the training data? Only randomly choose negative samples for the training to speed up. 
  How do you choose the negative samples ? 

* GloVe word vectors (v4) Not used much but simplicity [Pennington et al. 2014](https://www.aclweb.org/anthology/D14-1162)

 GloVe, global vectors for word representation. The model is to learn vector representors so that their inner products are good predictor for how often they are together.


## Applications using Word Embeddings

* Sentiment Classification (v1)

  Often you do not have enough labeled data. But word embeddings help.
  
  A simple average of the word vectors may be wrong in setiment classification. RNN may help.
  
* Debiasing word embeddings (v2) [Bolukbasi et al. 2016](https://arxiv.org/abs/1607.06520)

  Word embeddings can reflect gender, ethnicity, age, sexual orientation, and other biases of the text used to train the model.
 
  How to identify bias direction and neutralize, equalize pairs?
  

# Tips

* How to represent a word model?
* How to training a word model?
* How to speed up the training?

# Assignments

<!--* Training word vectors with Skipgram
-->
### Operations on word vectors - Debiasing

- Many operations such as cosine similarity or analogies can be applied to word vectors.
- Cosine similarity is the main metric to compare word vectors, although L2 distance may also be used.
- Your word vectors are learned by training a model on a dataset, they thus suffer from a bias inherent to the dataset.
- There are different debiasing methods given some words are bias-specific (need to be equalized) while others are non-bias-specific (need to be neutralized)

### Emojify

Attention: 
	
In `Emojify_v2`, please check the tips and documents of LSTM to make sure you understand. You should use the argument `return_sequences`. 

<font color='blue'>
**What we want you to remember from this notebook**:

- If you have a Natural Language Processing task, but not too much data, you can still build a strong model by using word vectors that have been trained on a large corpus.
- Word vectors give an incredible generatlization ability to your model, because the model can understand words it has never seen before thanks to how close their word vectors are to those of words it has seen in the training set.
- Building a Recurrent Neural Network for Sequence Classification in Keras is simple but tricky:
    - Inputs need to be indexes and padded up to a certain length.
    - To pretrain an `Embedding()` layer you have to set its weights to an embedding matrix.
    - `LSTM()` has a flag called `return_sequences` to decide if you would like to return every hidden states or only the last one.
    - It is common to use `Dropout()` right after `LSTM()`
- Reuse the code of this notebook to build Sentiment analysis applications for the industry, a few examples are:
    - Restaurant Reviews classification (how many start is this review?)
    - Movies Reviews classification
    - E-mails/Text-message/Tweets analysis (is this a kind email, or a funny email?)
    - Jokes (is this joke funny? This application can hopefully help you avoid some embarassing experiences...;))
    - ...    