## 基本数据类型
### int类型
为适应不同的情况，C语言提供了许多整数类型。整数类型可以表示不同的取值范围和正负值。

int类型是有符号类型，它的值必须是整数，可以是正负数和零，其取值范围因计算机系统而异。

#### 声明int变量
代码示例

    int name;
    int name1,name2;
  
> 变量获取值的方法
> 
> 1. 赋值。
> 
> 2. 使用函数。

#### 初始化变量
初始化变量为变量赋予一个初始值，可以在声明中完成。

代码示例

    int name = 5;
    int name1 = 25,name2 = 125;
    
#### 打印int值
代码示例

    #include <stdio.h>
    int main(void)
    {
        int ten = 10;
        int two = 2;
        
        printf("Doing it right:");
        printf("%d minus %d is %d\n",ten,2,ten-two);
        printf("Doing it wrong:");
        printf("%d minus %d is %d\n",ten,);
        
        return 0;
    }    

程序输出

    Doing it right:10 minus 2 is 8
    Doing it wrong:10 minus 16 is 1650287143
    
解释

在第二行输出中，由于未能给后两个%d转换说明符提供数值，所以打印出的是内存中的任意值。

引用书中原文。

> %d指明了在一行中打印整数的位置。%d称为转换说明，它指定了printf()应使用什么格式来显示一个值。
> 格式化字符串中的每个%d都与待打印变量列表中相应的int值匹配。
> 这个值可以是int类型的变量、int类型的常量或其他任何值为int类型的表达式。

#### 八进制和十六进制
在C语言中，使用特定的前缀表示进制。

十六进制的前缀为%OX或者%Ox，八进制的前缀为%O。

要显示特定的前缀，可以将以上表示为%#X,%#x,%#O。

代码示例

    #include <stdio.h>
    int main(void)
    {
        int num = 100;
        
        printf("dec=%d; octal=%o; hex=%x\n",num,num,num);
        printf("dec=%d; octal=%#o; hex=%#x\n",num,num,num);
        
        return 0;
    }
    
程序输出
    
    dec=100; octal=144; hex=64
    dec=100; octal=O144; hex=Ox64
    
#### 其它整数类型
为了适应不同的机器和情况，C语言还提供了其它的整数类型，这些整数类型有占用的存储空间以及表示的数值范围的不同。

其它整数类型有：short(短整型),long(长整型),long long(更大的取值范围), unsigned(只适用非负值)。

这些整数类型的声明和赋值均与int相同，不同的是执行打印函数语句时，所使用的转换说明符依次为%hd,%ld,%lld,%u。

因此，除了检查转换说明符是否有一一对应的数值，还要检查转换说明符的类型是否与待打印值的类型相匹配。

> 整数溢出
> 
> 当整数超过相应类型的取值范围时，将会重新从起始点（下界）开始。
> 
> 类似十二制的时钟，当超过12点时又变成从零开始。

