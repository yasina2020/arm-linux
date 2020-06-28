# win10、ubuntu、开发板三者互ping

<u>前提条件：开发板，win10都链接在同一个路由器上，开发板串口线连载pc上，pc上运行的虚拟机中跑ubuntu系统</u>

###### 1、win10选择wife连接至路由器A，通过cmd查询ip  （ipconfig）

![1593137710980](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593137710980.png)

###### 2、虚拟机设置：

​	用管理员权限打开虚拟网络编辑器

![1593138012927](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593138012927.png)

![1593137780794](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593137780794.png)

注意这里桥接到选择自己的电脑上的无线网卡名称

![1593137894345](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593137894345.png)

然后设置ubuntu的ip

![1593138101674](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593138101674.png)（自动分配即可）

###### 3、开发板网口用线连接到路由器A，开机

![1593138207678](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593138207678.png)

###### 4、验证

至此我们得到

win10ip，192.168.0.52

ubuntuip，192.168.0.53

开发板ip，192.168.0.51

互ping验证：

开发板ping：![1593138327288](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593138327288.png)

ubuntu ping：

![1593138385212](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593138385212.png)

win10 ping：

![1593138436352](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593138436352.png)



###### 5、补充

因为路由器A不一定能够上网，所以这样三者都无法上网，后期尝试通过路由器A桥接路由器B（主路由），来达到上网目的，方案研究中……