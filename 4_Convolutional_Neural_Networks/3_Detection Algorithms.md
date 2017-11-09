## Convolutional Neural Networks

* Object Localization and detection, what they are?
 * 区别图像分类（单个目标），图像定位（单个目标），图像探测（多个目标）。
 * label y = [pc, bc, by, bh, bw, c1, c2, ...], 左上角为(0, 0), x横坐标，y纵坐标
 * landmark detection，只输出目标位置
 
* Object Detection
 * sliding window method. 效率低！
 * 卷积实现sliding window method. ([Sermanet et al. 2014](https://arxiv.org/abs/1312.6229))
 * bounding box prediction ([Redmon et al. 2015 YOLO](https://arxiv.org/abs/1506.02640), hard to read! [Redmon et al. 2016](https://arxiv.org/abs/1612.08242)). How to define the bounding boxes?
 
* intersection over union. 重叠部分与预测和真实值和之间的比例，用来表征物体探测和好坏
* non-max suppression. 将同一物体的不同预测结果合并。具体步骤：去除所有pc小于0.6的box，while 剩下box， {找到最大的pc座位prediction，去除与该box的IoU大于0.5的其他box}。

* Anchor Boxes. 同时探测多个物体。 y = [anchor1 (pc bx by bh bw c1 c2 ..) anchor2 (...)   ....]

* YOLO Algorithm

* Region proposals ([Girshik et al. 2013](https://arxiv.org/abs/1311.2524), R-CNN, [Girshik 2015](https://arxiv.org/abs/1504.08083) Fast R-CNN, [Ren et al. 2016](https://arxiv.org/abs/1506.01497) Faster R-CNN)

要点：	
	
* 理解物体探测中的box的问题和方法。详细了解YOLO Algorithm.
* reference for YOLO model
	
 - Joseph Redmon, Santosh Divvala, Ross Girshick, Ali Farhadi - [You Only Look Once: Unified, Real-Time Object Detection](https://arxiv.org/abs/1506.02640) (2015)
 - Joseph Redmon, Ali Farhadi - [YOLO9000: Better, Faster, Stronger](https://arxiv.org/abs/1612.08242) (2016)
 - Allan Zelener - [YAD2K: Yet Another Darknet 2 Keras](https://github.com/allanzelener/YAD2K)
 - The official YOLO website (https://pjreddie.com/darknet/yolo/) 

* reference for ResNet model

 - Kaiming He, Xiangyu Zhang, Shaoqing Ren, Jian Sun - [Deep Residual Learning for Image Recognition (2015)](https://arxiv.org/abs/1512.03385)
 - Francois Chollet's github repository: [https://github.com/fchollet/deep-learning-models/blob/master/resnet50.py](https://github.com/fchollet/deep-learning-models/blob/master/resnet50.py)