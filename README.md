# Deliberately Vulnerable Android Hello World (DVAHW)

本应用基于Android开发者官方网站上的[Hello World应用](https://developer.android.com/training/basics/firstapp/index.html)教程和源代码，进行二次开发以满足[中国传媒大学移动互联网安全](http://sec.cuc.edu.cn/huangwei/wiki/teaching_mis.html)本科生课程``移动终端应用逆向分析``课内软件逆向、App签名等实验的需求。

目前支持的实验内容包括：

* Android应用程序的源代码基本结构和常用组件熟悉
    * 使用``SharedPreferences``持久化保存应用的私有数据和按需读取数据，了解数据被写入到文件系统上的``/data/data/<pkg name of app>/shared_prefs``的自定义``xml``文件，查看文件的属主和权限位设置与对应API使用方法
    * 使用``Intent``进行消息传递和启动``Activity``的基本方法
* APK打包和签名
* ``AndroidManifest.xml``配置实验
    * 在``AndroidManifest.xml``中添加权限声明后重新编译、打包应用并安装到模拟器中，查看应用的使用权限列表
* 使用[apktool](https://ibotpeaches.github.io/Apktool/)自动化反编译apk文件到源代码
    * 对比Java源代码和smali汇编代码之间的一一对应关系
    * 重打包实验
        * 修改源代码增加打印语句
        * 进行图标替换
        * 尝试安装重打包版应用到一台已经安装过原版应用的模拟器中，观察出错信息并解释原因
    * 使用``adb logcat``查看程序运行时的打印输出
* 通过逆向工程破解本应用的``注册序列号``算法
    * 信息反馈法
    * 特征函数法
    * 代码注入法


