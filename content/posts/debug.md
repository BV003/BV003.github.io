+++
title = 'Debug'
date = 2024-12-01T09:05:53+08:00
categories = ["技术"] 
tags = ["debug"]
+++

最近在做csapp的两个lab（bomblab和attacklab）
</br>发现debug还真的是好用

使用gdb，b打上相应的断点，run启动后，nexti进行单步调试，来查看相关的变量状态

```
(gdb) break (b)	在源代码指定的某一行设置断点，其中xxx用于指定具体打断点位置
(gdb) run (r）	执行被调试的程序，其会自动在第一个断点处暂停执行。
(gdb) continue (c）	当程序在某一断点处停止后，用该指令可以继续执行，直至遇到断点或者程序结束。
(gdb) next (n)	令程序一行代码一行代码的执行。
(gdb) step（s）	如果有调用函数，进入调用的函数内部；否则，和 next 命令的功能一样。
```

同时也感叹一下linux好用