## Convolutional Neural Networks

* Edge detection using convolution	
 * 卷积矩阵的值具体设置为多少？
 
* Padding	
 * no padding :  n - f + 1
 * padding : n + 2*p - f + 1
 * p = (f - 1) / 2
 * valid and same covolution
	
* strided convolution
 * step size, s
 * floor[ (n + 2p - f) / s + 1]
	
* convlolution over multi-dimensions
 *  conv for rbg images 
 *  add bias 
 *  10 filters with 3x3x3 parameter number: 280
	
* pooling layers
 * conv -> relu -> pooling -> fully connected -> softmax
 * no parameters to learn
 * max / average pooling.  f = 2, s = 2

* LeNet-5
 * neural network example / design
 * pattern, activation size, parameter size.
 
* Why convolutions?
 * parameter sharing.
 * sparsity of connections.

* programming assignments.
 * Convolutional Networks - Step by Step
 * Convolution model - Application

难点和关键点：		
   （1）理解卷积层的作用，为什么要用卷积层和pooling层。		
   （2）计算输出层的形状
   
   