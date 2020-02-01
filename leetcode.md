<!-- TITLE: Leetcode -->
<!-- SUBTITLE: A quick summary of Leetcode -->

# sort
## sort 比较
### c++ sort怎么实现的？
1. 小数据用插入排序
2. 大数据用quicksort
3. 为了防止递归过深导致stack爆掉，控制递归深度，达到一定深度后用headsort
4. https://zhuanlan.zhihu.com/p/36274119
### quicksort为什么比heap sort更加常用？
1. heapsort对缓存命中比较差

## 148 sort list
* 给2个无序的单向list，输出一个排好序的list, 要求nlogn 时间，常数空间
* 利用bottom up的merger sort来解决，注意分开函数来写
* 其实一开始想到了这样的做法，但是没有坚定信念，还是代码能力弱，有了想法不能很好的code出来，然后就放弃了，还是写的不够多