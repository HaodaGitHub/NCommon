# 公共组件使用说明

[TOC]

## 0.如何添加项目

* 首先拷贝源码到你的工程文件目录;
* 在你的项目 pro文件中添加:

```c
# import dll
win32: LIBS += -L$$PWD/../bin/ -lNCommon
DEPENDPATH += $$PWD/../bin

# import dll file
include($$PWD/../NCommon/NCommon_inc.pri)
```

** 具体的路径请按照你的项目情况进行修改**

## 1.如何使用

* 截取全屏并保存到本地

```
    qDebug()<<"*********************************截屏保存到本地测试开始******************************************";
    bool ret = NCommon::screenShotToFile();
    qDebug() << "是否保存到本地成功:" << ret;
    qDebug()<<"*********************************截屏保存到本地测试结束******************************************";
```

* 截取全屏保存到粘贴板

```
    qDebug()<<"*********************************截屏保存到粘贴板测试开始*****************************************";
    ret = NCommon::screenShotToClipBoard();
    qDebug() << "是否保存到粘贴板成功:" << ret;
    qDebug()<<"*********************************截屏保存到粘贴板测试结束*****************************************";
```

* 截取全屏后全屏显示

```
    qDebug()<<"*********************************截屏后并全屏显示测试开始*****************************************";
    ret = NCommon::screenShotToShow(2);
    qDebug() << "是否截取后全屏显示成功:" << ret;
    qDebug()<<"*********************************截屏后并全屏显示测试结束*****************************************";
```

* 部署APP程序

```
    qDebug()<<"*********************************发布APP脚本创建测试开始*****************************************";
    ret = NCommon::deployWindowsApp();
    qDebug() << "是否发布程序成功:" << ret;
    qDebug()<<"*********************************发布APP脚本创建测试结束*****************************************";
```

## 2. 组件路线图

* ~~1.截屏并保存到本地;~~
* ~~2.截屏并保存到粘贴板;~~
* ~~3.截屏后全屏显示;~~
* ~~4.部署APP程序;~~

## 3. changelog

* V1.0.1.0 初始化项目, 增加截屏保存到本地和粘贴板的功能;
* V1.0.2.0 增加截屏后全屏显示的功能;
* V1.0.3.0 增加程序部署的功能;
