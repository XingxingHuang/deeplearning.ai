## Face Recognition

* Face verification/ recognition 区别
* one shot learning. 
 * 只有一张图片来训练。
 * Learning "similarity" function: d(img1, img2)
* Siamese Network [Taigman et al. 2014](https://www.cs.toronto.edu/~ranzato/publications/taigman_cvpr14.pdf) Deepface
* Triplet Loss [Schroff et al. 2015](https://arxiv.org/abs/1503.03832) FaceNet
 * |F\_A - F\_P|^2 - |F\_A - F\_N|^2 > 0 - sig(margin)
 * given 3 images: L(A, P, N) = max(|A-P|^2 - |A-N|^2 + a, 0)

* Face Verifications [Taigman et al. 2014](https://www.cs.toronto.edu/~ranzato/publications/taigman_cvpr14.pdf) 

## Neural Style Transfer
* Content / Style / Generated image
* What ConvNets learning [Zeiler and Fergus 2013](https://arxiv.org/abs/1311.2901)  可视化神经网络，认识每层都学习什么内容
* Cost Function of Neural Style Transfer [Gatys et al. 2015](https://arxiv.org/abs/1508.06576) easy to read paper. J(G) = a J\_contest(C, G) + b J\_style(S, G)
 * content cost function, 看视频如何计算
 * style cost function, 看视频如何计算。 Define style as correlation between activations across channels.
 * 1D and 3D generalizations

 
--
 The Neural Style Transfer algorithm was due to Gatys et al. (2015). Harish Narayanan and Github user "log0" also have highly readable write-ups from which we drew inspiration. The pre-trained network used in this implementation is a VGG network, which is due to Simonyan and Zisserman (2015). Pre-trained weights were from the work of the MathConvNet team. 

- Leon A. Gatys, Alexander S. Ecker, Matthias Bethge, (2015). A Neural Algorithm of Artistic Style ([https://arxiv.org/abs/1508.06576](https://arxiv.org/abs/1508.06576)) 
- Harish Narayanan, Convolutional neural networks for artistic style transfer. [https://harishnarayanan.org/writing/artistic-style-transfer/](https://harishnarayanan.org/writing/artistic-style-transfer/)
- Log0, TensorFlow Implementation of "A Neural Algorithm of Artistic Style". [http://www.chioka.in/tensorflow-implementation-neural-algorithm-of-artistic-style](http://www.chioka.in/tensorflow-implementation-neural-algorithm-of-artistic-style)
- Karen Simonyan and Andrew Zisserman (2015). Very deep convolutional networks for large-scale image recognition ([https://arxiv.org/pdf/1409.1556.pdf](https://arxiv.org/pdf/1409.1556.pdf))
- MatConvNet. [http://www.vlfeat.org/matconvnet/pretrained/](http://www.vlfeat.org/matconvnet/pretrained/)

--
- Florian Schroff, Dmitry Kalenichenko, James Philbin (2015). [FaceNet: A Unified Embedding for Face Recognition and Clustering](https://arxiv.org/pdf/1503.03832.pdf)
- Yaniv Taigman, Ming Yang, Marc'Aurelio Ranzato, Lior Wolf (2014). [DeepFace: Closing the gap to human-level performance in face verification](https://research.fb.com/wp-content/uploads/2016/11/deepface-closing-the-gap-to-human-level-performance-in-face-verification.pdf) 
- The pretrained model we use is inspired by Victor Sy Wang's implementation and was loaded using his code: [https://github.com/iwantooxxoox/Keras-OpenFace](https://github.com/iwantooxxoox/Keras-OpenFace).
- Our implementation also took a lot of inspiration from the official FaceNet github repository: [https://github.com/davidsandberg/facenet](https://github.com/davidsandberg/facenet)