###一个C语言日志库###

#### 简介:
这是用C语言写的日志库，兼容 windows与linux，欢迎大家给出意见。

#### 接口函数：
程序的接口为 `LR_LOG(const char *file, int line, int level, int status, const char *fmt, ...)`函数，调用此函数，传入参数。

#### 函数说明：
1. file	: 文件名称
2. line	: 行号
3. level	: 错误级别
	- 0 -- 没有日志
	- 1 -- debug级别
	- 2 -- info级别
	- 3 -- warning级别
	- 4 -- err级别
4. status: 错误码
5. fmt	: 可变参数(用于LOG信息)

#### 用法
1. WinNT先在C盘根目录建立lrlog文件夹，Linux则在用户目录建立log文件夹
2. 将logrecord.h与logrecord.c添加至项目，引入头文件logrecord.h(#include "logrecord.h")
3. 调用LR_LOG函数即可
