<!-- TITLE: Config Page -->
<!-- SUBTITLE: 各种关于安装 在新的机器上配置自己原先的开发环境的东西 -->

# Header

## Linux
### apt包管理
1. apt默认是国外源 非常慢 可以采用换源（使用清华的源）来下载
2. 具体的操作流程为备份原先的source.list，在清华大学TUNA官网发布的[Ubuntu 镜像使用帮助](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)中到对应的源，替换原先的source.list，sudo apt-get update更新即可
3. [参考流程](https://segmentfault.com/a/1190000012572571)
4. 还可以安装apt-fast 多线程下载