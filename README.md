# c-code

#define _CRT_SECURE_NO_WARNINGS//一定要加在源文件的第一行，它是用来忽略一些系统对不安全函数的警告的。比如scanf

#include <stdio.h>

#include <string.h>



//包含一个叫stdio.h的文件
//std-标准 standard input output


//mian函数前面的int表示mian函数调用返回一个整数值
//int main()//称为主函数，也是程序的入口。
//{
	//prinf是库函数
	//库函数-c语言本身提供给我们使用的函数
	//使用别人的东西要打招呼
	//#include
	//printf("hello world\n");
	//return 0;//返回0，也叫返回整数
	//}

//知识点！！！

//char-字符类型
//%d - 打印整数
//%c - 打印字符
//%f - 打印浮点数字
//%p - 以地址的形式打印
//%x - 打印16进制数字
//%s - 打印字符串
//键盘上能敲出来的所有东西都是字符包括空格。
// |--按位或--意思是只要有一个值为1则结果为1。
// ^--按位异或--规律是对应的二进制位相同，则为0；对应的二进制位不同，则为1.
//&--按位与--意思是只要有一个值为0则结果为0
//sizeof--用于计算大小。例如sizeof(int), sizeof(a).
//*--解引用操作符
//(exp1>exp2?exp1:exp2)--三相操作符
//struct--结构体
//arr exp []--数组



//bit //比特位，最小单位，2进制，一个比特位可以存放八个0或1.
// 
// 
//int main()
//{
//	char ch = 'A'; //内存
//	printf("%c\n", ch);//%c--打印字符格式的数据
//	int age = 20;
//	printf("%d\n", age);//%d--打印整形十进制的数据
//	//shotr int--短整型
//	//int--整型
//	//long--长整型
//	long num = 100;
//	printf("%d\n", num);
//	//long long--超长整型
// 
//  //short age = 20; //向内存申请两个字节的空间，用来存放20
//  //float weight = 64.2f; //必须在数字后面加上f，不然则会把float识别成double
//
//	return 0;
//}
//
//	


//int num = 20;//(全局变量，定义在{}之外的变量，{}也被称为代码块。
//int main()
//{
//	int num = 10;//局部变量，定义在代码块（{}）的变量。
//	//建议局部变量与全局变量不要使用同一个名字，容易误会，产生bug
//	//当局部变量的名字与全局变量一样的话，优先使用局部变量。
//	printf("%d\n", num);
//	return 0;
//}


//int main()
//{
//	//计算两个数的和
//	int num1 = 0;
//	int num2 = 0;
//	int sum = 0;
//	//所有的变量定义都需要放在代码块的最前面，否则会报错。
//	//输入数据，使用输入函数scanf
//	scanf("%d%d", &num1, &num2);//选取地址符号&
//	sum = num1 + num2;
//	printf("sum = %d\n", sum);
//	return 0;
//}

//常量

//int main()
//{
//	////const//意思为常属性，用于将变量转换成常量。
//	//const int num1 = 10;//--n是变量，但是又有常属性，我们把n叫做常变量。
//	//printf("%d\n", num1);
//	//
//
//
//
//	return 0;
//}
////

//#define MAX 2//写在mian函数的外面
////#defien--定义的标识符常量
//int main()
//{
//	int arr[MAX] = { 0 };
//	printf("%d\n", MAX);
//
//	return 0;
//}


////枚举常量

////枚举关键--enum
//enum Name
//{
//	YI,
//	ER,
//	SAN,
//	SI,
//	WU
//};
//int main()
//{
//	enum Name name = YI;
//	printf("%d\n", name);
//	printf("%d\n", ER);
//	printf("%d\n", SAN);
//	printf("%d\n", SI);
//
//	return 0;
//}


//字符串用“”来表达
//字符需要使用''
//转义字符--\--用于消除某些具有特殊意义的字符的意义，使其变成普通字符。
//int main()
//{
//	char arr[] = "\"c:test / 32 / test.c\"";
//	printf("%s\n", arr);
//	//--/t--水平制表符
//	//--\0--结尾
//	//--\n--换行
//	//printf("%d\n", strlen(arr));
//	//printf("%c\n", 's');
//	printf("%c\n", '\99');
//	return 0;
//}


//if语句运用

//int main()
//{
//	int input = 0;
//	printf("加入比特");
//	printf("好好学习(1/0)");
//	scanf("%d", &input);
//	if (input == 1)
//		printf("给你一个好offer\n");
//	else
//		printf("烤红薯\n");
//
//
//	return 0;
//}


//while语句运用

//int main()
//{
//	int line = 0;
//	printf("加入比特\n");
//	while (line<2000)
//	{
//		printf("敲一行代码\n");
//		line++;
//
//	}
//	printf("走向人生巅峰\n");
//
//	return 0;
//}

//自定义函数的运用

//int add(int a, int b)
//{
//	int o = a + b;
//	return o;
//}
//int main()
//{
//	int num4 = 10;
//	int num5 = 20;
//	int sum = 0;
//	sum = add(num4, num5);
//	printf("sum = a+b = %d\n", sum);
//
//	return 0;
//}

//综合使用例子1

//int Add(int x, int y, int c)
//{
//	int z = (x + 100) * (c * y);
//	return z;
//}
//int main()
//{
//	int input = 0;
//	printf("加入比特(0/1)>:");
//	scanf("%d", &input);
//	if (input == 1)
//	{
//		printf("开始学习。选择你的学习天数\n");
//		int num1 = 100;
//		int num2 = 200;
//		int num3 = 2;
//		int sum = 0;
//		scanf("%d%d%d", &num1, &num2, &num3);
//		sum = Add(num1, num2, num3);
//		while (sum > 1)
//		{
//			printf("学习中:%d小时\n", sum);
//			if (sum < 1000000)
//			{
//				sum++;
//				
//			}
//			else
//				if (sum == 100000)
//				{
//					printf("小目标\n");
//					sum = 1;
//					
//				}
//				else
//				{
//					printf("走向人生巅峰\n");
//					sum = 1;
//					
//				}
//		}
//		sum = Add(num1, num2, num3);
//		printf("恭喜你，成功毕业，拿到好offer");
//		printf("月薪 = %d元\n", sum);
//	}
//	else
//		printf("回家烤红薯！！！");
//
//
//	
//	return 0;
//}

//求两个数的较大值

//int main()
//{
//	int a = 0;
//	int b = 0;
//	printf("对比两个数的大小\na = ");
//	scanf("%d", &a);
//	printf("对比两个数的大小\nb = ");
//	scanf("%d", &b);
//	if (a > b)
//		printf("答案是a, a = % d\n", a);
//	else
//		printf("答案是b, b = %d\n", b);
//
//	return 0;
//}

//int Max(int x, int y)
//{
//	
//	if (x==y)
//		printf("数值一样");
//	else
//		if (x > y)
//			return x;
//		else
//			return y;
//	
//}
//int main()
//{
//	int a = 20;
//	int b = 10;
//	int max = 0;
//	printf("对比两个数的大小\na = ");
//	scanf("%d", &a);
//	printf("对比两个数的大小\nb = ");
//	scanf("%d", &b);
//	max = Max(a, b);
//	printf("较大值为：%d\n", max);
//	return 0;
//}

//sizeof与arr（数组）的运用

//int main()
//{
//	int a = 1;
//	int arr[] = { 1,3,4,6,7,};
//	printf("%d\n", sizeof a);//大小为4，因为该变量被存放于整形（int）之中。
//	printf("%d\n", sizeof(int));//大小为4，因为整形（int）大小为4。
//	printf("%d\n", sizeof(arr));//大小为20，因为这里计算的是整个数组的大小，该数组里有五个数，每个数被存放于int之中所以大小为4*5=20.
//	printf("%d\n", sizeof(arr) / sizeof(arr[0]));
//	return 0;
//}

//符号使用

//int main()
//{
//	int a = 10;
//	int b = a++;
//	printf("a = %d\nb = %d\n", a, b);//11，10
//	//后置++，是先使用，++。
//	b = ++a;
//	printf("a = %d\nb = %d\n", a, b);
//	//前置++，先++，后使用。
//	//--与++的使用规则相同。
//
//
//	int c = 0;//四个字节，32个比特位。=00000000000000000000000000000000
//	int d = ~c;//b是有符号的整形（当它是符号的整形时，第一个数字则是符号位。0表示正，1表示负）。=10000000000000000000000000000001（这里的第一个1表示为负号）
//	//~--按（2进制）为反取符。
//	//00000000000000000000000000000000
//	//11111111111111111111111111111111
//	//原码，反码，补码
//	//负数在内存中存储时，储存的是2进制的补码。
//	//00000000000000000000000000000000（原码）
//	//11111111111111111111111111111111
//	printf("%d\n", d);//使用的，打印的是这个数的原码。
//	//原码符号位不变（也就是第一个数字），其余取反，得到反码，反码加1，得到补码。
//	//补码加1，得到反码，其余取反，符号位不变，得到原码。
//	return 0;
//}

//int main()
//{
//	int num1 = 200;
//	int num2 = 2000;
//	int max = 0;
//	max = (num1 > num2 ? num1 : num2);//（exp?exp2:exp3)条件操作符，也叫三目操作符。
//	//如果前面式子成立，则第一个变量会成为整个式子的变量，如果不成立，则第二个变量成为式子的变量。
//	printf("%d\n", max);
//	
//	return 0;
//}

//int add(int x, int y)
//{
//	int z = 0;
//	z = x + y;
//	return z;
//}
//int main()
//{
//	int arr[] = { 0 };//[]--下标引用操作符
//	int arr1[] = { 1,2,3 };
//	//此处1，2，3对应的下标分别是0，1，2 。也就是说下标是从0开始的。
//	int num1 = 10;
//	int num2 = 20;
//	int sum = 0;
//	sum = add(num1, num2);//()--函数调用操作符。
//	printf("%d\n", sum);
//
//	return 0;
//}


//常见关键字

//int main()
//{
//	auto int num1 = 0;//局部变量，自定变量。
//	register int num2 = 1;//建议把怒num2定义成寄存器变量。（当一个变量成为寄存器变量时，他的读取速度会变得非常快。）
//	signed int num3 = 2;//有符号变量--正或者负。
//	//int定义的变量是有符号的。
//	unsigned int num4 = 2;//无符号变量--没有正负之分，全部都是正数。
//
//
//	return 0;
//}

//1 //static修饰局部变量
//	//局部变量的生命周期延长。
//2 //static修饰全局变量
//  //改变全局变量的作用域
//  //让静态的全局变量只能够在自己的源文件内使用，出了源文件就没法再使用了。
//3 //static修饰函数
//  //改变函数的作用域（不准确）
//  //改变函数的链接属性
//  //外部链接==》内部链接
// 
//int test()
//{
//	//static--静态操作符
//	static int e = 1;//a是一个静态的局部变量。
//	e++;
//	printf("e = %d\n", e);
//	//当没有static的时候答案为2，2，2，2，2
//	//当有了static的时候答案为2，3，4，5，6
//
//
//}
//int main()
//{
//	int i = 0;
//	unsigned int o = 20;
//	typedef unsigned int u_int;//这里将unsigned int 重定义成 u_int，也就是说它们的用途是一样的。
//	//typedef--符号重定义符
//	u_int t = 12;
//	while (i < 5)
//	{
//		test();
//		i++;
//	}
//
//	return 0;
//}
//
//int main()
//{
//	//extern--声明外部符号（引用其他源文件里所定义的变量。）
//	extern int g_test;
//	printf("%d\n", g_test);
//	//当其他源文件里的变量没有使用static时，能够成功引用
//	//当其他源文件里的变量使用static时，不能引用。
//	return 0;
//}
//
//extern int add(int, int);//使用声明外部符号来引用源文件外的函数。
//int main()
//{
//	int num1 = 2;
//	int num2 = 20;
//	int sum = 0;
//	sum = add(num1, num2);
//	printf("sum = %d\n", sum);
//	return 0;
//}





