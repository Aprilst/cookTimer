# Funcs

+ 实现定时开
+ 实现定时关
+ device开关状态检测
+ 温度检测
+ 电池电量检测
+ 显示屏
+ 输入开关
+ Web Server
+ 发送提醒信息

# Process

1. 长按 开机

   ​	初始化各个sensor：DS18B20，光敏value初始化，舵机位置归零；

​			显示时间，电量；

旋钮？设置定时开始时间；

confirm

设置定时结束时间；

confirm

倒计时开始 -> 

​	time is up -> 开启工具（舵机）

​	检测是否开启 -> send msg | Succeed or Failed

倒计时1开始 ->

​	time is up1 - > 调小挡位？/ 关闭？ 

​	检测对应操作是否成功 -> send msg 

-----------------------------------------------------

使用过程，持续检测设备的开启状态；

如果有异常需要send msg;

---------------------------------------------------------

...

doing nothing...Or Close? (close only when device is off)