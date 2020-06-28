# 蓝牙模块AT调试

<u>蓝牙版本</u>

<u>BOLUTEK Firmware V2.2, Bluetooth V2.1</u>

1、如何进入at模式

​	蓝牙断电，en引脚接高电平，蓝牙上电接usb to tll ，en高电平断开（或接低电平），打开串口调试助手，即可进入at模式

![1593304451686](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593304451686.png)

发送：at+version查看版本号

![1593304523884](C:\Users\84590\AppData\Roaming\Typora\typora-user-images\1593304523884.png)

其他指令如下：

at+name<paral>

at+default

at+reset

at+pin<prarl>

at+baud<paral>

更多指令参考<http://www.doc88.com/p-282362565002.html>



