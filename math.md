<!-- TITLE: Math -->
<!-- SUBTITLE: A quick summary of Math -->

#  Linear Algebra 

## Jacobian矩阵
1. 一阶偏导数以一定方式排列成的矩阵, 行列式称为雅可比行列式


![Jacobian](/uploads/jacobian.png "Jacobian")

## Cholesky 分解
1. [wiki说明](https://zh.wikipedia.org/wiki/Cholesky%E5%88%86%E8%A7%A3)
2. [简单直接的blog](https://www.qiujiawei.com/linear-algebra-11/)



# Optimization

## 非线性优化
### 高斯牛顿
1. 泰勒展开 转换为线性优化 不断迭代求解
2. [高斯牛顿](https://blog.csdn.net/tywwwww/article/details/77720360)

### L-M
1. 相比高斯牛顿，引入一个\lambda I(I 为正定矩阵)加入到步长更新上
2. 控制步长 根据情况调整迭代速度
3. 同时泰勒展开的并不一定有解 引入\lambda I解决这个问题
4. [L-M](https://blog.csdn.net/tywwwww/article/details/77720360)


### 拉格朗日乘子法
1.  [深入理解拉格朗日乘子法（Lagrange Multiplier) 和KKT条件](https://blog.csdn.net/lijil168/article/details/69395023)
2.  条件的限制通过对待定系数求导＝０来控制

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