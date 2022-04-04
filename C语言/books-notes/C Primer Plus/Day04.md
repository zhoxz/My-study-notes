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
