<!-- TITLE: Math -->
<!-- SUBTITLE: A quick summary of Math -->

#  Linear Algebra 

## Jacobian矩阵
1. 一阶偏导数以一定方式排列成的矩阵, 行列式称为雅可比行列式
![Jacobian](/uploads/jacobian.png "Jacobian"){.align-center}

## Cholesky 分解
1. [wiki说明](https://zh.wikipedia.org/wiki/Cholesky%E5%88%86%E8%A7%A3)
2. [简单直接的blog](https://www.qiujiawei.com/linear-algebra-11/)

# other fun code

## 点到矩形的最短距离
1. [stackexchange](https://gamedev.stackexchange.com/questions/44483/how-do-i-calculate-distance-between-a-point-and-an-axis-aligned-rectangle)

```
If (x,y) is the centre of the rectangle, the squared distance from a point (px,py) to the rectangle's border can be computed this way:

dx = max(abs(px - x) - width / 2, 0);
dy = max(abs(py - y) - height / 2, 0);
return dx * dx + dy * dy

If that squared distance is zero, it means the point touches or is inside the rectangle.
```