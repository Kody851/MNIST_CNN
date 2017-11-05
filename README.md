# 简单的CNN实现MNIST

## 1、网络设置

* 使用两个卷积层（每个卷积层后接一个池化层）、一个全连接层的卷积神经网络。

* mini-batch为50，迭代20000次；

* 使用Dropout层防止过拟合，训练时保留50%的节点

## 2、结果分析

* 测试集上准确率为0.9931
* 找出分错的样例
https://www.oreilly.com.cn/ideas/?p=838
https://github.com/wagonhelm/NaNmnist
（caffe实现）：http://blog.csdn.net/tianrolin/article/details/53542050
![Example.png](https://github.com/Kody851/MNIST_CNN/blob/master/Example.png)

## 3、convolution kernel 的可视化
使用 Tensorboard
