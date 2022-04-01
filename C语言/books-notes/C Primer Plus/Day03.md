## 简单程序的结构
1. 程序由一个或多个函数组成，必须有main()函数。
2. 函数由函数头和函数体组成。
3. 函数头包括函数名、传入该函数的信息类型和函数的返回类型。
4. 函数体由花括号包围起来，由一系列语句声明组成。

一个简单的C程序格式

    #include <stdio.h>
    int main(void)
    {
        语句；
        return 0;
    }
    
## 提高程序可读性的技巧
1. 选择有意义的函数名。
2. 编写注释。
3. 在函数中用空行分隔概念中的多个部分。
4. 每条语句只占一行。

## 进一步使用C
    
    // fathm_ft.c--把英寻转换为英尺
    #include <stdio.h>
    int main(void)
    {
        int feet,fathoms;
        
        fathoms = 2;
        feet = 6 * fathoms;
        printf("There are %d feet in %d fathoms!\n",feet,fathoms);
        printf("Yes,I said %d feet!\n",6*fathoms);
        
        return 0;
    }
    
输出如下

    There are 12 feet in 2 fathoms!
    Yes,I said 12 feet!
    
## 多个函数

    /* two_func.c--一个文件里包含两个函数 */
    #include <stdio.h>
    void butlet(void); /* 声明函数原型（函数声明） */
    int main(void)
    {
        printf("I will summon the butler function.\n");
        butler(); /* 函数调用 */
        printf("Yes.Bring me some tea and writeable DVDs.\n");
        
        return 0;
    }
    void butler(void) /* 函数定义,是函数本身的源代码 */
    {
        printf("You rang, sir?\n");
    }
    
输出如下
    
    I will summon the butler function.
    You rang, sir?
    Yes.Bring me some tea and writeable DVDs.
    
## 调试程序
程序的错误通常被称为bug，找出并修正错误的过程叫做调试（debug）。
### 一个错误的程序

    /* nogood.c--有错误的程序 */
    #include <stdio.h>
    int main(void)
    (
        int n,int n2,int n3;
        
        /* 该程序有多处错误
        n = 5;
        n2 = n * n;
        n3 = n2 * n2;
        printf("n = %d, n squared = %d, n cubed = %d\n",n,n2,n3)
        
        return 0;
    )
