循环语句

int main()
{
	int a = 0;

	while (a < 100)
	{ 
		if (a == 50)
			continue;//终止本次循环后面的所有内容，并从头开始新的一轮循环
		if (a == 90)
			break;//停止后期所有的循环，直接终止所有的循环。
		printf("学习%d\n", a);
		a++;
	}

	return 0;
}

int main()
{
	int a = 0;
	//EOF--en of file--文件结束标志（-1）
	//下面的代码可以通过输入ctrl+z来结束，crtl+z=EOF
	while ((a=getchar()) != EOF)
	{
		putchar(a);
		printf("%c\n", a);
	}

	return 0;
}

int main()
{
	int a = 0;
	char ch = 0;
	char password[20] = { 0 };
	printf("输入密码>:\n");
	scanf("%s", &password);
	while ((ch = getchar()) != '\n');//用于消除读取缓存区里剩余的字符，避免影响到下面其他代码的读取。
	{
		;//空语句
	}
	printf("请确认:>(Y/N)\n");
	a = getchar();
	if (a == 'Y')
		printf("输入成功\n");
	else
		printf("取消输入\n");
}

for语句
int main()
{
	int a = 0;
	//   初始化；判断  ；调整 
	for (a = 1; a <= 10; a++)
	{
		if (5 == a)
			continue;//这里的判断如果成立，则会跳过下面的代码从（调整）部分开始执行，而不会像while语句一样从头再来，导致死循环。
		//while语句会导致死循环是因为（调整）部分在continue下面，所以会导致死循环，但是for语句的（调整）部分并没有在continue下面，所以不会死循环。
		printf("%d\n", a);
	}
	return 0;
}

int main()
{
	//每当遇到for循环时，电脑会先把for循环运行完在运行下一行代码。
	//也就是说，当for循环嵌套时，会先将里面的for先运行完，再运行外面的for
	//这导致此行代码的结果为100个呵呵。而不是10个或是20个。
	int a = 0;
	for (; 10 > a; a++)
	{ 
		int b = 0;
		//当然也可以把定义放在for循环里面，这样同样也会打印一百次。
		for (; 10 > b; b++)//需要在表达式里放入a=0，否则只会打印十次
			printf("呵呵\n");
	}

	return 0;
}

int main()
{
	int a = 0;
	int b = 0;
	for (a = 0, b = 0; 2 > a && 5 > b; a++, b++)
		//for语句里可以存在多个变量，以及其他操作符，例如&&（逻辑与）和||（逻辑或）
		printf("呵呵");
	return 0;
}

int main()
{
	int a = 0;
	int c = 0;
	for (a = 0, c = 0; a = 0; a++, c++)
		//这里的答案为一次都不运行
		//判断表达式被赋值为0
		//0为假，所以直接结束循环
		//如果被赋值成非0，则是死循环。
		printf("呵呵");
	return 0;
}

int main()
{
	for (;;)//for语句表达式可以为空
		//当判断表达式为空时，判断恒为真。
		printf("呵呵");
	return 0;
}

计算n的积乘
int main()
{
	int n = 0;
	int ret = 1;
	scanf("%d", &n);
	int a = 0;

	for (a=1;a<=n; a++)
	{
		
		ret = ret * a;
	}
	printf("%d\n", ret);
		
	return 0;
}

计算1！-10！的乘积
int main()
{
	int n = 0;
	int ret = 1;
	int sum = 0;
	scanf("%d", &n);
	int a = 0;
	
	

	for (a = 1; a <= n; a++)
	{

		ret = ret * a;
		
		sum = sum + ret;
	}
	printf("%d\n", sum);

	return 0;
}

如何查找数组中的无序元素
int main()
{
	int arr[] = { 1,3,5,6,7,8,10,13,17 };
	int a = 13;//这个数为上标
	
	int size = sizeof(arr) / sizeof(arr[0]);
	int left = 0;//左下标
	int right = size - 1;//右下标

	while (left <= right)
	{
		int mid = (right + left) / 2;//这个书为下标。
		if (arr[mid] > a)
		{
			mid变量里的数只是下标，而a是上标，并且我们要找的是上标，所以要使用arr[mid]来表示上标。
			right = mid - 1;
			假设变量a小于mid，则表明a不在mid往右的数组里，所以右边可以变成现在的mid-1，缩小范围。
			为什么是mid-1？因为如果是a=mid，则直接输出结果了。
		}
		
		else if (arr[mid] < a)
		{
			left = mid + 1;
		}
		else
		{
			printf("找到了，下标 = %d\n", mid);
			break;
		}
	}
	if (left > right)
	{
		printf("无法找到该数的下标");
	}
	return 0;
}

int main()
{
	int a = 3;
	int b = a+1;
	int c;
	c = a * b;
	printf("%d", c);
	return 0;
}

求最大公约数（辗转相除法）
int main()
{
	int a = 0;
	int b = 0;
	int c = 0;
	scanf("%d%d", &a, &b);
	while (c = a % b)
	{
		a = b;
		b = c;
	}
	printf("%d\n", b);
	
}

求1000年到2000年之间的闰年。
int main()
{
	int a = 1000;
	while (1000 <= a && 2000 >= a)
	{
		if (a % 4 == 0)
			if (a % 100 != 0)
				printf("闰年%d\n", a);
		if (a % 400 == 0)
			printf("闰年%d\n", a);
		a++;
		
	}
		
	return 0;
}
