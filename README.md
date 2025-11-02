# class
c language
1.the first note
like now i am ready to make a summary of my learn recently
such as the base language please say "hello"
the C is -  include <stdio.h> // this is a the look-ahead for instructions
 int/整行 main 主函数 （）
 { 
   printf("hello\n");
   return 0;返回值
   }
2.the second note 
// is 行批注 称作转义字符  /*  */可多行进行批注
\n is function is 换行(pay attention to its point)
question:两数相加
code is ()
#include (stdio.h)
int main()
{
    int a,b,sum;
    a=123;
    b=456;
    sum=a+b;
    printf("a+b=%d\n",sum) ;
    return 0;
}
questions and what you need to know 
1..程序是什么 为什么要设计程序 程序=算法+结构 
2..了解程序基本结构（顺序结构 选择结构 循环结构‘whilde 当....  until..... 直到’） 根据各种描述算法的语言对程序进行描述 （自然语言，伪代码,流程图等）
3..语言有：计算机语言 编译语言 高级语言 C语言属于高级语言，C语言是面向底层代码的语言 不同于python java等面向对象的语言 C语言中的结构和语法需要严密遵循基本的运算逻辑（顺序结构，选择结构，循环结构）
4..是否理解预指令的含义 以及对于函数类型的理解 int long float char ..... 
CARE
1.. int main 与 void main区别  int main()和int main(void)的区别
2..各个函数结尾的终止符号
3..对数据的定义
4..计算机运行的逻辑与矛盾点
the mind and way
1..分析问题类型 需求 列出具体的算法描述
2..写出大体的 函数 结构 运算方法
3..检查bug 改进 运行
2025.10.23
4..变量的说明 x=x+1 前面的x为变量空间 后面为变量值 如：理解 令 x=x+y; y=x-y; x=x-y; 谁先被赋值谁先被破坏即原变量被覆盖但赋值的变量原变量没有变 可理解为copy
5..对数据的定义可以int x,y,z; 然后再 x=...; y=....; z=.....; 也可以int x=... ,y=.....,z=.....;
6..传统流程图 ns流程图 开始（起始框） 处理符号 判断符号 输入输出符号 结束（） 连接点 注释框 流程线
7..homework 画n-s流程图 理解变量
8..%d十进制整数 %d将光标移至下一个Tab位
scratch  内变量的定义 多变量的使用 询问并等待 
最近作业 碰撞小球的碰撞次数 通过缩放变量值将小猫的大小放大缩小 将x和y值交换 z=x;x=y;y=z;理解变量值的交换而不是表面的值交换（错误如***printf("....",x,y);printf("....",y,x);）\\
11.2
1..对于函数或变量的定义加深 如 int a; a=2; //  char a; a='a';单个字符用单引号，系统对于单个字符的显示为ascall值，%d则是值，%c则是把值对应的字符打印出来如用printf.%d十进制整数 %s字符串
%c字符 %f 浮点型数字   doubel float 双精度浮点型 单精度浮点型 %1f代表小数点1位 %f则是没有小数点
2..字符串的定义 char a[]=""；中括号可以写内容代表范围（暂时对此概念不确定）双引号内是字符
3..在赋值的顺序是从右往左，正常运算则是从左至右，除了加减乘除。%是求余 对于符号的理解，i++是先取i值再逐步加1，++1则是先加1取i值.减号则同理；
定义常量 #define PI 3.14       或者是const 数据类型 常量名 如 const float pi=3.14f    3.14f表示该数值为单精度浮点型
int 4个字节 float 4个字节 double 8个字节   char占1个字节
4..测量字节占用 sizeof(char)
********************#include<stdio.h>
int main()
{
	int a,b,c;
	a = 10;
	b = 20;
	c = (a > b ? a : b);//三目运算符 先对判断条件进行判断a>b 如果符合则c=a不符合则c=b
	printf("%d", c);
	return 0;
}
/*
******************************switch语句  switch()参数只能是整形变量 逻辑 case'1'若输入1则执行case'1'
如case'1':
printf("ok\n");
break;switch遇到break中断
注意default:
printf("no\n")如果上面的情况都不满足则执行此条
c=getchar()；//为从键盘的输入缓冲区一个一个取走一个字符 如输入abc\n则会依次取得a ,b , c , \n 这四个字符
当读取正常字符时候会将字符转为ASCLL码
它的返回值是整形
*/



/**********************if语句  
if()
{
}
如  int main()
{
	 int a=1;
	 int b=2;
	 if(a>b)
	   {
	     printf("%d\n");
	   }
	return 0;
 }
********************* if else 语句
 如 int main()
{
	int a=1;
	int b=2;
	if(a>b)
 {}
 else
 {}
 return 0;
}
****************if-else if-else 语句
if()
{}
else if()
{}
else
{}
练习c=(A>b?A:b)   if(){} //  if(){}  // if(){}else{}   //if(){} else(){}  else{} //switch()  case'': printf()? break;
********************while语句
while和if一样是有判断的 和三目运算符也相似需要while()进行判断 然后当符合这个判断的时候进行{}如果不符合则停止
和switch语句不一样的是 switch()语句需要用case'':来进行判断如果符合则 printf("")然后执行完则break停止，即结束并跳出switch语句 ，如果不加break 则程序不会进行二次判断直接输入以下各个判断结果，由此显示，3种判断为顺序判断且执行一次则输出以下内容不停止且以下判断无效；
********************do...while语句 
do做什么{} 执行括号内的程序while（）直到不符合while的判断条件停止；
*********************for循环
for(初始值；判断条件；初始值的运行方式)
{
sum+=i;//意思为 sum=sum+i;
}
printf("sum=%d\n",sum);
嵌套循环 各种循环语句之间可以相互嵌套





