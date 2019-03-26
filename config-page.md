<!-- TITLE: Config Page -->
<!-- SUBTITLE: 各种关于安装 在新的机器上配置自己原先的开发环境的东西 -->



# Linux
## apt包管理
1. apt默认是国外源 非常慢 可以采用换源（使用清华的源）来下载
2. 具体的操作流程为备份原先的source.list，在清华大学TUNA官网发布的[Ubuntu 镜像使用帮助](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)中到对应的源，替换原先的source.list，sudo apt-get update更新即可
3. [参考流程](https://segmentfault.com/a/1190000012572571)
4. 还可以安装apt-fast 多线程下载
5. [没有sudo权限怎么apt-get install](https://unix.stackexchange.com/questions/42567/how-to-install-program-locally-without-sudo-privileges) 非常麻烦，下载源码，编译安装，下载依赖，更新环境变量

## Idconfig
1. 更新动态链接库，默认搜寻/lilb和/usr/lib，以及配置文件/etc/ld.so.conf内所列的目录下的库文件。 lib*.so*
2. [相关说明](https://blog.csdn.net/chenzixun0/article/details/56278632)
3.  [linux ldconfig命令,环境变量文件配置详解](https://blog.csdn.net/winycg/article/details/80572735)

### LD_LIBRARY_PATH
1. [what-is-the-difference-between-path-and-ld-library-path](https://unix.stackexchange.com/questions/44990/what-is-the-difference-between-path-and-ld-library-path)
2.  动态库的查找路径

# install some tools
## install opencv
1. [install opencv](https://blog.csdn.net/cocoaqin/article/details/78163171)
2. /etc/ld.so.conf.d 下为动态库的指定文件 [/etc/ld.so.conf.d的作用&动态库](https://blog.csdn.net/apn172/article/details/8868968)
3. 