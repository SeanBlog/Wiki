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
4. 注意 htop默认会将thread也当成独立的process来显示，和ps -AL一样，同时thread之间切换很快，你无法确定是哪个在工作，可以按H显示main process，反应整个process占的资源等[Why are there many processes listed under the same title in htop?](https://superuser.com/questions/118086/why-are-there-many-processes-listed-under-the-same-title-in-htophttps://superuser.com/questions/118086/why-are-there-many-processes-listed-under-the-same-title-in-htop)
### scp use regression
1. 需要scp "sevrver@ip:ssssss" xxxx
2. [How to scp with regular expressions](https://unix.stackexchange.com/questions/67055/how-to-scp-with-regular-expressions)


### export
1. Linux export命令用于设置或显示环境变量。export可新增，修改或删除环境变量。export的效力仅及于该次登陆操作
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

### mac
1. [mac address](https://en.wikipedia.org/wiki/MAC_address)
2. [mac spoofing](https://en.wikipedia.org/wiki/MAC_spoofing)

### ifconfig in mac
1. [Mac OS X ifconfig命令解释](https://blog.csdn.net/yangziluomu/article/details/75043171)

### DHCP
1. [INSTALLING AND CONFIGURING DHCP](https://www.dummies.com/programming/certification/installing-and-configuring-dhcp/)
2. DHCP handles all this work automatically. Each client gets a unique IP address, subnet mask, and other IP information such as default gateways and the IP addresses of WINS (Windows Internet Name Service) and DNS (Domain Name System) servers. DHCP makes certain that no clients have duplicate addresses, and this entire process is invisible to network administrators and network users. 
