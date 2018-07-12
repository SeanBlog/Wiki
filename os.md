<!-- TITLE: OS&Network -->
<!-- SUBTITLE: Operation System and Network -->

# OS
## File System
### soft link vs hard link
1. 硬链接是指向同一个inode
2. 软链接的数据部分指向原文件的file name 
3. [一个详细的说明](https://www.ibm.com/developerworks/cn/linux/l-cn-hardandsymb-links/index.html)
4. 图片示例 

![Pic 1](/uploads/pic-1.png "Pic 1"){.align-center}



## Linux commond
### htop
1. 升级版本的top
2. 功能更多 更加好用
3. 监听线程，cpu，disk，memory，/搜索命令，u选择用户，根据cpu等排序


# Network
## basic concept
1. [一个蛮不错的blog](http://www.cnblogs.com/JuneWang/p/3917697.html)
### ip
1. ip 地址=网络地址+主机地址

### DNS 服务器
1. 域名和IP一一对应
2. 将域名转换为对应的IP

### subnet mask 
1. 判断电脑是否属于同一个子网，是的话 可以通信
2. 将子网ip与子网掩码做and操作后，如果一样的话，为同一个网络可以通信。

### gateway
1. 不同网络通信的设备
2. 可以是路由器、或三层交换机、防火墙

![Gateway](/uploads/gateway.jpg "Gateway"){.align-center}
