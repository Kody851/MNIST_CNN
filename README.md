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
 
pycharm报错 ：

2017-11-05 02:36:20.515076: I tensorflow/stream_executor/dso_loader.cc:129] Couldn't open CUDA library libcupti.so.8.0. LD_LIBRARY_PATH: 
2017-11-05 02:36:20.515109: F ./tensorflow/stream_executor/lib/statusor.h:205] Non-OK-status: status_ status: Failed precondition: could not dlopen DSO: libcupti.so.8.0; dlerror: libcupti.so.8.0: cannot open shared object file: No such file or directory
bash: line 1:  4092 Aborted                 (core dumped) env "PYTHONUNBUFFERED"="1" "PYTHONPATH"="/home/kody851" "PYCHARM_HOSTED"="1" "JETBRAINS_REMOTE_RUN"="1" "PYTHONIOENCODING"="UTF-8" /usr/bin/python -u /home/kody851/new0/TensorBoard.py
 
命令行 ：

kody851@fit16:~$ tensorboard -- logdir=F:/pycharm/projects1102/new0/logs/mnist_with_summaries
Traceback (most recent call last):
  File "/usr/local/bin/tensorboard", line 11, in <module>
    sys.exit(main())
  File "/usr/local/lib/python2.7/dist-packages/tensorflow/tensorboard/tensorboard.py", line 203, in main
    tb = create_tb_app(plugins)
  File "/usr/local/lib/python2.7/dist-packages/tensorflow/tensorboard/tensorboard.py", line 105, in create_tb_app
    raise ValueError('A logdir must be specified. Run `tensorboard --help` for '
ValueError: A logdir must be specified. Run `tensorboard --help` for details and examples.
