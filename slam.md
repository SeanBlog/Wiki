<!-- TITLE: Slam -->
<!-- SUBTITLE: A quick summary of Slam -->


# Resource
1. 半闲居士在国内的SLAM领域的地位毋庸置疑，他的blog上有一些他整理和维护的资源[resource](https://www.cnblogs.com/gaoxiang12/p/5762702.html)
2. **SLAM非常经典的公开课** 看完基本上视觉SLAM应该比较清楚了[泡泡机器人公开课](http://rosclub.cn/post-1065.html)



# 基本知识
## 相机模型
1.[相机内参矩阵](https://www.cnblogs.com/Jessica-jie/p/6596450.html)
2.相机畸变
* 	[相机标定之畸变矫正与反畸变计算](https://www.cnblogs.com/mafuqiang/p/8134617.html)
*   [opencv 去畸变源代码实现](https://github.com/opencv/opencv/blob/master/modules/calib3d/src/undistort.cpp)

## 三角化测量深度
1. [对极几何基本概念](https://blog.csdn.net/tina_ttl/article/details/52749542#3-%E5%AF%B9%E6%9E%81%E5%87%A0%E4%BD%95%E7%9A%84%E5%87%A0%E4%B8%AA%E7%9B%B8%E5%85%B3%E6%A6%82%E5%BF%B5)
2. [三角化---深度滤波器](http://www.mamicode.com/info-detail-2061030.html)

## Kalman filter

[Kalman filter wiki](https://en.wikipedia.org/wiki/Kalman_filter)

# PnP问题
1. 已知对应的2D和3D点 求解相机姿态（R,T）
2. [泡泡公开课对应视频-PnP 算法简介&代码解析-柴政](http://rosclub.cn/post-566.html)

## P3P
1. 选取4组对应关系
2. 利用三组对应关系和三角形余弦定理 构建方程
3. 吴氏消元法 最多四组解
4. 最后一个点 代入 选择重投影误差最小的解
![P 3 P](/uploads/p-3-p.png "P 3 P")

## EPnP


# 经典框架
## ORB-SLAM
### online course

1. [泡泡公开课对应视频-ORB-SLAM2源码详解-吴博](http://rosclub.cn/post-505.html)
2. [泡泡公开课对应视频-orb-slam的简单讲解-冯兵](https://www.bilibili.com/video/av7102994)

### ORB Feature point
1. ORB抽取FAST特征点，使用Rotate BUREF 作为描述算子(解决旋转不一致性，利用描述patch的质心和特征点连线确定方向)，再利用Harris corner选取前几个特征点。
[Opencv Intro](https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_feature2d/py_orb/py_orb.html)



# ROS
[ros code simple api](http://wiki.ros.org/rosbag/Code%20API)
[add custom msg](http://wiki.ros.org/ROS/Tutorials/CreatingMsgAndSrv)