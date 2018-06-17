<!-- TITLE: Cplusplus -->
<!-- SUBTITLE:杂七杂八 学过丢掉 用过忘记 突然记起来的点 -->

### Struct VS Class

1. 	Class 默认data和function是private的 struct默认是public的
2.  其他的还有一些类class的特性的区别（比如construct function,destruction function） 不过关键是第一点
3.  [ref](https://stackoverflow.com/questions/54585/when-should-you-use-a-class-vs-a-struct-in-c)
4.  何时使用struct或者class？
 * 针对POD type的数据 采用struct，其他的采用class 
 * 如果数据要求是private的从使用clas
5. 什么是POD：
* A Plain Old Data Structure in C++ is an aggregate class that contains only PODS as members, has no user-defined destructor, no user-defined copy assignment operator, and no nonstatic members of pointer-to-member type. 
* [ref]( <https://stackoverflow.com/questions/146452/what-are-pod-types-in-c> )