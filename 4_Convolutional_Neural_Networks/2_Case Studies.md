## Case Studies

* classic networks:
	* LeNet-5 [LeCun et al., 1998](http://www.dengfanxin.cn/wp-content/uploads/2016/03/1998Lecun.pdf) can skip. conv+pool+fc structure.
	* AlexNet [Krizhevsky et al., 2012](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf) deeper, relu, max-pooling, GPU, local response normalization.  GOOD ONE TO READ.
	* VGG-16 [Simonyan & Zisserman 2015](https://arxiv.org/abs/1409.1556) simple structure, conv+conv+pool+...
	* ResNet [He et al., 2015](https://arxiv.org/abs/1512.03385) help to train deeper. why? (一个视频的讲解)
	* Inception [Szegedy et al. 2014](https://arxiv.org/abs/1409.4842) 1x1 convolution why?
	
	视频中对模型有很多细节的讲解，这些经典文章用过一些现在不常用的技能	1x1 convolution [Lin et al. 2013](https://arxiv.org/abs/1312.4400)
	
## Practice Questions
* Using open-source implementation. Why? How?
* Transfer Learning. 
 * Freeze first few layers depending on the size of training data
* Data augmentation. 
 * Increase the performance by pre-reduce the data. Mirroring, Random Cropping(isn't perfect), Rotation, Shearing, Local warping ..., Color Shifting, PCA color.
* more data vs hand-engineering. 
    * While less data, hand hacking is more important
    * Tips for doing well on benchmarks: Ensembling, Multi-crop at test, use open source code  
