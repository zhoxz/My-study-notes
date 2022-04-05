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

### 八进制和十六进制
在C语言中，使用特定的前缀表示进制。

十六进制的前缀为%OX或者%Ox，八进制的前缀为%O。

要显示特定的前缀，可以将以上表示为%#X,%#x,%#O。
