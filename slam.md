<!-- TITLE: Slam -->
<!-- SUBTITLE: A quick summary of Slam -->

# Header

## Resource
1. 半闲居士在国内的SLAM领域的地位毋庸置疑，他的blog上有一些他整理和维护的资源[resource](https://www.cnblogs.com/gaoxiang12/p/5762702.html)
2. **SLAM非常经典的公开课** 看完基本上视觉SLAM应该比较清楚了[泡泡机器人公开课](http://rosclub.cn/post-1065.html)


## 三角化测量深度
1. [三角化---深度滤波器](http://www.mamicode.com/info-detail-2061030.html)

## PnP问题
1. 已知对应的2D和3D点 求解相机姿态（R,T）
2. [泡泡公开课对应视频-PnP 算法简介&代码解析-柴政](http://rosclub.cn/post-566.html)

## ORB-SLAM
### online course

1. [泡泡公开课对应视频-ORB-SLAM2源码详解-吴博](http://rosclub.cn/post-505.html)
2. [泡泡公开课对应视频-orb-slam的简单讲解-冯兵](https://www.bilibili.com/video/av7102994)

### ORB Feature point
1. ORB抽取FAST特征点，使用Rotate BUREF 作为描述算子(解决旋转不一致性，利用描述patch的质心和特征点连线确定方向)，再利用Harris corner选取前几个特征点。
[Opencv Intro](https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_feature2d/py_orb/py_orb.html)

## Kalman filter

[Kalman filter wiki](https://en.wikipedia.org/wiki/Kalman_filter)

## ROS
[ros code simple api](http://wiki.ros.org/rosbag/Code%20API)