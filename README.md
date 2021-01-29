# vs2013-1-29
#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>

int main()
{
	int a = 0;
	char b = 'w';
	int arr[10] = { 0 };

	printf("%d\n", sizeof(a));//4
	printf("%d\n", sizeof(int));//4

	printf("%d\n", sizeof(b));//1
	printf("%d\n", sizeof(char));//1

	printf("%d\n", sizeof(arr));//40
	printf("%d\n", sizeof(int [10]));//40

	return 0;
}

int main()
{
	short s = 0;
	int a = 10;
	printf("%d\n", sizeof(s = a + 5));//2
	printf("%d\n", s);//0
	return 0;
}

int main()
{
	int a = 0;
	//~ 按(2进制)位取反
	//00000000000000000000000000000000 - 补码
	//11111111111111111111111111111111 - 反码
	//10000000000000000000000000000001 - 原码
	//-1
	printf("%d\n", ~a);

	return 0;
}

int main()
{
	int a = 11;
	a = a | (1 << 2);
	printf("%d\n", a);//15
	a = a&(~(1 << 2));
	printf("%d\n", a);//11

	//00000000000000000000000000001011
	//00000000000000000000000000000100
	//1<<2;
	//00000000000000000000000000000001
	//
	//00000000000000000000000000001111
	//11111111111111111111111111111011
	//00000000000000000000000000000100
	//00000000000000000000000000001011
	//
	return 0;
}

int main()
{
	int a = 10;
	printf("%d\n", ++a);//前置++，先++，后使用

	return 0;
}

int main()
{
	int a = 10;
	printf("%d\n", a++);//后置++。先使用，再++

	return 0;
}

int main()
{
	int a = (int)3.14;
	
	return 0;
}

int main()
{
	int a = -10;
	int* p = MULL;
	printf("%d\n", !2);
	printf("%d\n", !0);
	a = -a;
	p = &a;
	printf("%d\n", sizeof(a));
	printf("%d\n", sizeof(int));
	printf("%d\n", sizeof a);//ok
	printf("%d\n", sizeof int);//no

	return 0;
}

//sizeof和数组
void test1(int arr[])
{
	printf("%d\n", sizeof(arr));//(2) 4
}
void test2(char ch[])
{
	printf("%d\n", sizeof(ch));//(4) 4
}
int main()
{
	int char[10] = { 0 };
	char ch[10] = { 0 };
	printf("%d\n", sizeof(arr));//(1) 40
	printf("%d\n", sizeof(ch)); //(3) 10
	test1(arr);
	test2(ch);

	return 0;
}

int main()
{
	int a = 3;
	int b = 5;
	int c = a&&b;
	printf("%d\n",c);
	return 0;
}

int main()
{
	int a = 0;
	int b = 5;
	int c = a&&b;
	printf("%d\n", c);
	return 0;
}

int main()
{
	int a = 3;
	int b = 5;
	int c = a||b;
	printf("%d\n", c);
	return 0;
}

int main()
{
	int a = 0;
	int b = 0;
	int c = a||b;
	printf("%d\n", c);
	return 0;
}

int main()
{
	int i = 0;
	int a = 0;
	int b = 2;
	int c = 3;
	int d = 4;
	i = a++ && ++b && d++;
	printf("a=%d\n", a);
	return 0;
}

int main()
{
	int i = 0;
	int a = 1;
	int b = 2;
	int c = 3;
	int d = 4;
	i = a++ && ++b && d++;
	printf("a=%d\n", a);
	return 0;
}

int main()
{
	int i = 0;
	int a = 1;
	int b = 2;
	int c = 3;
	int d = 4;
	i = a++ || ++b || d++;
	printf("a=%d\n", a);
	return 0;
}

int main()
{
	int i = 0;
	int a = 0;
	int b = 2;
	int c = 3;
	int d = 4;
	i = a++ || ++b || d++;
	printf("a=%d\n", a);
	return 0;
}

int main()
{
	int a = 0;
	int b = 0;
	if (a > 5)
	{
		b = 3;
	}
	else
	{
		b = -3;
	}
	return 0;
}

int main()
{
	int a = 0;
	int b = 0;
	b = (a > 5 ? 3 : -3);
	return 0;
}

int main()
{
	int a = 10;
	int b = 20;
	int max = 0;
	if (a > b)
	{
		max = a;
	}
	else
	{
		max = b;
	}
	return 0;
}

int main()
{
	int a = 10;
	int b = 20;
	int max = 0;
	int max(a > b ? a : b);
	return 0;
}

int main()
{
	int a = 1;
	int b = 2;
	int c = (a > b, a = b + 10, a, b = a + 1);//逗号表达式
	return 0;
}

int main()
{
	int a = 0;
	int b = 0;
	int c = 0;
	int d = 0;
	if (a = b + 1, c = a / 2, d > 0)
		printf("%d\n", hehe);
	return 0;
}

int main()
{
	a = get_val();
	count_val(a);
	while (a > 0)
	{
		//业务处理
		a = get_val();
		count_val(a);
	}
	return 0;
}

int main()
{
	a = get_val();
	count_val(a);
	while (a = get_val(),count_val(a), a > 0)
	{
		//业务处理
	
	}
	return 0;
}

int main()
{
	int arr[10];//创建数组；
	arr[9] = 10;//实用下标引用操作符
	return 0;
}

int get_max(int x, int y)
{
	return x > y ? x : y;
}

int main()
{
	int a = 10;
	int b = 20;
	//调用函数的时候的（）就是函数调用操作符
	int max = get_max(a, b);
	printf("max=%d\n", max);
	return 0;
}

//学生
//int float
//
//创建一个结构体类型-struct Stu
struct Stu
{
	char name[20];
	int age;
	char id[20];
		
};
int main()
{
	int a = 10;
	//使用struct Stu这个类型创建了一个学生对象s1，并初始化
	struct Stu s1 = { "张三", 20, "2019010305" };
	printf("%s\n", s1.name);
	printf("%s\n", s1.age);
	printf("%s\n", s1.id);
	//结构体变量.成员名
	return 0;
}

struct Stu
{
	char name[20];
	int age;
	char id[20];

};
int main()
{
	int a = 10;
	//使用struct Stu这个类型创建了一个学生对象s1，并初始化
	struct Stu s1 = { "张三", 20, "2019010305" };
	struct Stu* ps = &s1;
	printf("%s\n", (*ps).name);
	printf("%d\n", (*ps).age);
	return 0;
}

struct Stu
{
	char name[20];
	int age;
	char id[20];

};
int main()
{

	int a = 10;
	//使用struct Stu这个类型创建了一个学生对象s1，并初始化
	struct Stu s1 = { "张三", 20, "2019010305" };
	struct Stu* ps = &s1;
	printf("%s\n", ps->name);
	printf("%d\n", ps->age);
	return 0;
}

struct Stu
{
	char name[10];
	int age;
	char sex[5];
	double score;

};
void ste_age1(struct Stu stu)
{
	stu.age = 18;
}
void ste_age2(struct Stu* pStu)
{
	pStu->age = 18;//结构成员访问
}
int main()
{
	struct Stu stu;
	struct Stu* pStu = &stu;//结构成员访问

	stu.age = 20; //结构成员访问
	set_age1(stu);

	pStu->age = 20;//结构成员访问
	set_age2(pStu);
	return 0;
}

int main()
{
	char a = 3;
	//0000000000000000000000000000011
	//00000011 - a
	//
	char b = 127;
	//0000000000000000000000001111111
	//01111111 - b
	//
	//a和b如何相加
	//0000000000000000000000000000011
	//0000000000000000000000001111111
	//0000000000000000000000010000010
	//
	char c = a + b;
	//10000010 - c
	//1111111111111111111111110000010 - 补码
	//1111111111111111111111110000001 - 反码
	//1000000000000000000000001111110 - 原码
	//-126
	printf("%d\n",c);
	return 0;
}

int main()
{
	char a = 0xb6;
	short b = oxb600;
	int c = 0xb60000000;
	if (a == 0xb6)
		printf("a");
	if (a == 0xb600)
		printf("b");
	if (a == 0xb6000000)
		printf("c");
	return 0;
}

int main()
{
	char c = 1;
	printf("%u\n", sizeof(c));//1
	printf("%u\n", sizeof(+c));//4
	printf("%u\n", sizeof(!c));//1
	return 0;
}









