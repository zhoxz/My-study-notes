# 初识数据类型
使用变量或者函数需要声明其数据类型，数据类型决定了其数据的存储大小和存储方式。
## 基本数据类型
* char：字符数据类型。
* short：短整型。
* int：整型。
* long：长整型。
* long long：更长的长整型。
* float：单精度浮点数。
* double：双精度浮点数。
* void：表示无类型。

代码示范：

    int main(){
        char ch="a";
        int num=20;
        short num1=9;
        float num2=5.200;
        return 0;
    }    

## 数据类型的大小
sizeof:关键字，计算类型或者变量所占的空间大小。

代码示范：

    #include <stdio.h>
    int main(){
        printf("%d\n",sizeof(char));
        printf("%d\n",sizeof(short));
        printf("%d\n",sizeof(int));
        printf("%d\n",sizeof(long));
        printf("%d\n",sizeof(long long));
        printf("%d\n",sizeof(float));
        printf("%d\n",sizeof(double));
        //  %d:表示打印一个整数。
        //  \n:换行。
        
        return 0;
    }

输出结果：


解释：

sizeof的单位是字节（byte）。

计算机采用二进制。

计算机的单位是比特位（bit）。

* 1byte=8bit
* 1kb=1024byte=2^10byte
* 1mb=1024kb
* 1gb=1024mb
* 1tb=1024gb
* 1pb=1024tb
