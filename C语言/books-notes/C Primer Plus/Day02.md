# 第二章 C语言概述
## 一个简单的C语言示例

    #include <stdio.h>
    int main(void){
        int num;
        num = 1;
        
        printf("I am a simple ");
        printf("computer.\n");
        printf("My favorite number is %d because it is first.\n",num);
        
        return 0;}
        
程序输出

    I am a simple computer.
    My favorite number is 1 because it is first.
    
> 如果程序运行窗口一闪而过，可以在return前添加一行代码，
> 
> 该代码将让程序等待击键，才会关闭窗口。

    getchar（）；

