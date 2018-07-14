<!-- TITLE: Code -->
<!-- SUBTITLE: A quick summary of Code -->

# Intro


# C++
## Struct VS Class

* Class 默认data和function是private的 struct默认是public的
* 其他的还有一些类class的特性的区别（比如construct function,destruction function） 不过关键是第一点 [ref](https://stackoverflow.com/questions/54585/when-should-you-use-a-class-vs-a-struct-in-c)
* 何时使用struct或者class？
	* 针对POD type的数据 采用struct，其他的采用class 
	* 如果数据要求是private的从使用clas
* 什么是POD：
* A Plain Old Data Structure in C++ is an aggregate class that contains only PODS as members, has no user-defined destructor, no user-defined copy assignment operator, and no nonstatic members of pointer-to-member type.  [ref]( <https://stackoverflow.com/questions/146452/what-are-pod-types-in-c> )

## Stack VS heap VS static

* Stack 高地址 编译器自己管理
* Heap 低地址 malloc new之类的 程序员管理 不然内存泄漏
* Static:全局变量和静态变量(initialized data那里)

![2](/uploads/2.png "2")

## vector 的push_back的数据传递
* [relater problem](https://stackoverflow.com/questions/2275076/is-stdvector-copying-the-objects-with-a-push-back)

```text
C++ 11
void push_back (const value_type& val);
void push_back (value_type&& val);

C++ 98
void push_back (const value_type& val);
```

* C++ 中的vector中存储的是拷贝的变量，但是你存进去的时候是以const T &的，避免多次拷贝（The object you push is passed by reference to avoid extra copy. Then a copy is placed in the vector.）
* 可以看[stackoverflow的一个回答](https://stackoverflow.com/questions/11762474/c-stl-vector-push-back-taking-reference)：

The other option would be
void push_back(T x);
that is, taking x by value. However, this would (in C++03) result in creating an extra copy of x(the copy in the arguments to push_back). Taking x by const reference avoids this.
Let's look at the stack for a call v.push_back(T()) taken by value:
```text
v.push_back(T());                      // instance of T
void std::vector<T>::push_back(T x)    // copy of T
new (data_[size_ - 1]) T(x)            // copy of copy of T
```

Taking by const reference we get:
```text
v.push_back(T());                             // instance of T
void std::vector<T>::push_back(const T &x)    // const reference to T
new (data_[size_ - 1]) T(x)                   // copy of T
```

In C++11 it would be possible (though unnecessary) to take x by value and use std::move to move it onto the vector:
```text
v.push_back(T());                             // instance of T
void std::vector<T>::push_back(T x)           // copy of T
new (data_[size_ - 1]) T(std::move(x))        // move the copy of T
```


# Git

## git solve conflict
1. git diff看冲突在哪里
2. 修改冲突代码
3. 再commit即可 

## git branch
1. dev branch针对需求开发
2. 解决后再合并到master，合并后删除无用branch（太多会影响认别）
3. [example1](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001375840038939c291467cc7c747b1810aab2fb8863508000) [廖雪峰](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/001375840038939c291467cc7c747b1810aab2fb8863508000)

## git hook
1. git push 或者pull触发相关脚本
2. 可用来提交简单的代码到服务器或者其他线上
3. [例子](https://ma.ttias.be/simple-git-push-workflow-deploy-code-server/)
4. [基本语法](https://git-scm.com/book/zh/v2/%E8%87%AA%E5%AE%9A%E4%B9%89-Git-Git-%E9%92%A9%E5%AD%90)


## git init vs git init --bare
1. git init --bare创建的是git的裸库 没有work tree，只有.git里面的版本信息
2. 常用来做中央版本库或者git服务器（其实就是规定没有人可以在上面git add.之类的，只允许push or pull）
3. [What is the difference between “git init” and “git init --bare?](https://stackoverflow.com/questions/7861184/what-is-the-difference-between-git-init-and-git-init-bare)
4. [How do you use “git --bare init” repository?](https://stackoverflow.com/questions/7632454/how-do-you-use-git-bare-init-repository)

## --work-tree --git-dir
1. git-dir指定的是.git所在目录（保存版本信息）
2. work-tree是工作区，通常是和.git所在同级目录的源码
3. git --git-dir=file-system-folder/.git --work-tree=file-system-folder checkout existing-branch(切换file-system-folder到file-system-folder/.git中的existing-branch)

## git submodule
1. project 里面有project
2. [相关介绍](https://git-scm.com/book/zh/v2/Git-%E5%B7%A5%E5%85%B7-%E5%AD%90%E6%A8%A1%E5%9D%97)
```
git submodule add  //添加 
git submodule init  //初始化注册
git submodule update  //clone submodule project

```