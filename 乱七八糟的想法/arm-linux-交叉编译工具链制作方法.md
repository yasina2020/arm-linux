# arm-linux-交叉编译工具链制作方法

制作交叉编译工具链一般通过crosstool或者crosstool-NG工具

本文使用后者，其需要先配置安装，才能使用，如何配置和安装也是敢问要解决的任务。

准备工作：Ubuntu 18.04.4 LTS、

##### **1、安装crosstool-NG****

###### 下载crosstool-NG、



![1593064891764](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593064891764.png)

（网速感人）

###### 解压和创建后需要用到的目录

![1593065117060](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593065117060.png)

安装制作交叉编译工具链必备的软件

virtualbox复制黏贴问题![1593065344144](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593065344144.png)![1593065331306](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593065331306.png)

![1593065316748](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593065316748.png)

然后安装蹭墙工具，重启即可

delors@delors-VirtualBox:~$ sudo apt-get install sed bash cut dpkg-dev patch texinfom4 libtool statwebsvn tar gzip bzip2 lzmabison flex texinfo automakelibtool 

配置整个工程并进行依赖检查

![1593066733138](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593066733138.png)

发现缺少很多软件，一个一个安装

![1593066873982](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593066873982.png)

重复安装-检查（可能要很多次）

缺少libtool后，sudo apt-get install libtool后依然提示缺少libtool则需要再安装sudo apt-get install libtool-bin

缺少![1593068184675](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593068184675.png)安装sudo apt-get install libncurses5-dev

![1593068878159](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593068878159.png)

<u>**这里还缺少几个东西 但找不到解决办法，但是检查依赖可以通过，先暂时不管</u>*****



###### win10

ip; 192.168.1.11

子网掩码 255.255.255.0

网关 192.168.1.1

dns 192.168.1.1

###### ubuntu

ip; 192.168.1.12

子网掩码 255.255.255.0

网关 192.168.1.1

dns 192.168.1.1

###### 开发板  u-boot

ip; 192.168.1.13

子网掩码 255.255.255.0

网关 192.168.1.1

dns 192.168.1.1

###### 开发板 linux