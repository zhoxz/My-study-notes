> [学习链接:https://www.bilibili.com/video/BV1cq4y1U7sg?p=4](https://www.bilibili.com/video/BV1cq4y1U7sg?p=4).
# 初始C语言
## 什么是C语言
C语言是一门面向过程的、抽象化的通用程序设计语言，广泛应用于底层开发。C语言能以简易的方式编译、处理低级存储器。
C语言是仅产生少量的机器语言以及不需要任何运行环境支持便能运行的高效率程序设计语言。尽管C语言提供了许多低级处理
的功能，但仍然保持着跨平台的特性，以一个标准规格写出的C语言程序可在包括类似嵌入式处理器以及超级计算机等作业平台
的许多计算机平台上进行编译。

最新的C语言标准是C18。
> 来自百科
## 创建我的第一个C语言项目
工具：准备一个得心应手的编译器，我使用的是Dev++。其它编译器还有Clang、GCC、MSVC、vs等。

步骤：
1. 创建一个项目。（类似文件夹）
2. 创建源文件，可以有多个源文件。（xxx.c---源文件、xxx.h---头文件）
3. 编写代码。
4. 编译代码。

在屏幕上打印“hello，world！”。

代码：

    #include <stdio.h>
    int main(){
        printf("hello,world!");
        return 0;
    }  
    //函数体  
    
解释：
* int：表示函数返回类型，是整型的意思。
* main：是函数名，函数名可以自定义，但是每个项目必须包含一个main（主函数）。C语言从主函数的第一行开始执行。
* printf：是库函数，用于在屏幕输出信息，使用时需引用stdio.h头文件。
* { }内的是函数体。
* //是注释，注释语句不会执行和出现。

效果显示：

![](https://github.com/zhoxz/My-study-notes/blob/main/C%E8%AF%AD%E8%A8%80/image/hello.jpg?raw=true)
