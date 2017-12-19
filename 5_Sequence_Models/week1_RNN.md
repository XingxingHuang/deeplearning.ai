# week1

* sequence data (v1): speech recognition, music generation, sentiment classification, DNA sequence analysis, Machine translation, Video activity recognition, name entity recognition.

* How to representing words?  one hot encode is one. (v2)		
* Why not a standard networks? (v3)

```
lengths of inputs and outputs change.
doesn't share features learned across different positions of text.
```

* How to backpropagation through time? (v4) not quite different

* Different tyopes of RNNs. (v5) input and output may have different types/ lengths. many-to-many, one-to-many, many-to-one, one-to-one.

* How to make language model and sequence generation. (v6) basic idea.

* **Vanishing Gradients with RNN** (v7) This is a common problem in very deep neural networks. The ouput in RNN has stronger influrence from the closer words.  Solutions are **GRU** (v8), **LSTM** (V9).

* Understand GRU ([Cho et al, 2014](https://arxiv.org/abs/1409.1259) and [Chuang et al, 2014](https://arxiv.org/abs/1412.3555)) and LSTM ([Hochreiter et al. 1997](http://www.bioinf.jku.at/publications/older/2604.pdf), hard to read!) and draw them (v8, v9). Understand the equation to calculate the memory and gates. Understand full GRU vs simple GRU ![](https://image.slidesharecdn.com/nlpdl06forslideshareenghelvetica-160706022723/95/recent-progress-in-rnn-and-nlp-5-638.jpg?cb=1467843604)

* Further read. Bidirectional RNN (v10), Deep RNNs (v11). 

# Tips

* (v3) 两种展示RNN的方法，在很多文章中，采用[fold的方式](http://www.wildml.com/wp-content/uploads/2015/09/rnn.jpg)。但是这种方式有时候比较难理解，可以尝试展开后理解。
* (v3) RNN有一个问题，由于每次只是用前面的知识，所以仍然会有一定限制。
* (v8, v9) 详细介绍了精髓 GRU 和 LSTM，花时间自己画一画结构，写出公式会非常帮助理解。
* (v9) LSTM 对GRU进行了优化。除了本身的update gate，还包括 forget gate， output gate。
* Bidirectional RNN 解决了序列中预测可能同时与前后都有关系的问题。

# Assignment
### Building a recurrent neural network - step by step (2h)
	
### Character-Level Language Modeling (1h)
**References**:

- To see the results of a slightly more complicated model, check out andrej karpathy's [blog post](http://karpathy.github.io/2015/05/21/rnn-effectiveness/).

- This notebook has been highly inspired and has used code from Andrej Karpathy's implementation: https://gist.github.com/karpathy/d4dee566867f8291f086

### Music Generation using RNN with LSTM (1h)