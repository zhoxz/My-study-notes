# 第三章 数据和C
## 示例程序

    #include <stdio.h>
    int main(void)
    {
        float weight; /* 你的体重 */
        float value; /* 相等重量的白金价值 */
        
        printf("Are you worth your weight in platinum?\n");
        printf("Let is check it out.\n");
        printf("Please enter your weight in pounds: ");
        
        /* 获取用户输入 */
        scanf("%f",&weight);
        /* 假设白金价值为每盎司$1700 */
        /* 14.5833用于将英镑常衡盎司转化为金衡盎司 */
        value = 1700.0*weight*14.5833;
        printf("Your weight in platinum is worth $%.2f.\n",value);
        printf("You are easily worth that! If platinum prices drop,\n");
        printf("eat more to maintain your value.\n");
        
        return 0;
    }
    
### 错误与警告
错误表示程序中有错，不能进行编译。

警告表示编写的代码有效，但可能不是预期情况，仍可继续编译。

### 程序输出

    Are you worth your weight in platinum?
    Let is check it out.
    Please enter your weight in pounds: 156
    Your weight in platinum is worth $3867491.25.
    You are easily worth that! If platinum prices drop,
    eat more to maintain your value.
    
### 程序调整

如代码一闪而过，这时候需要调用两次getchar（）函数。

### 程序解释
* 浮点数类型变量(float)可以处理更大范围的数据，可以存储带小数的数字。
* 在printf()中使用%f来处理浮点值。%.2f中的.2用于精确控制输出，指定输出的浮点数只显示小数点后面两位。
* scanf()函数用于读取键盘的输入。%f说明scanf()要读取用户从键盘输入的浮点数，&weight告诉scanf()把输入的值赋给名为weight的变量。scanf()函数使用&符号表明找到weight变量的地点。

## 变量与常量数据
常量：已经预先设置好的，不会发生变化的固定的值称为常量。

变量：在程序运行的过程中，有可能进行二次赋值或者更改的称为变量。

引用书中原文
> 有些数据类型在程序使用之前已经预先设定好了，在整个程序的运行过程中没有变化，这些称为常量（constant）。其他数据类型在程序运行期间可能会改变或被赋值，这些称为变量（variable）。在示例程序中，weight是一个变量，14.5833是一个常量。

## 数据：数据类型关键字
C通过识别一些基本的数据类型来区分和使用这些不同的数据类型。如果数据是常量，编译器一般通过用户书写的形式来识别类型（如，42是整数，42.100是浮点数）。但是，对变量而言，要在声明时指定其类型。

通过关键字创建的类型，按计算机的存储方式可以分为两大基本类型：整数类型和浮点数类型。

### 位、字节和字
位、字节和字是描述计算机数据单元或存储单元的术语。这里主要指存储单元。

位(bit)：是最小的存储单元，可以存储0或1，用以表示计算机的开与关，是计算机内存的基本构建块。

字节(type):是常用的计算机存储单位，1字节为8位。1位可以存储0或者1，因此1字节等于八位，可以存储256(2^8)种不同的0或者1的组合。

字(word)：是设计计算机时给定的自然存储单位。计算机的字长越大，其数据转移越快，允许的内存访问也更多。

### 整数和浮点数

* 整数没有小数部分，浮点数有小数部分。
* 浮点数可以表示的范围比整数大。
* 对于一些算术运算，浮点数损失的精度更多。
