# lesson 1
## c#基础
1.输出
```c-sharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            string message;//定义string变量
            message = Console.ReadLine();//接收输入的值赋值给变量
            Console.WriteLine(message);//输出
            Console.ReadKey();//输出停留，等待按键结束
        }
    }
}

```
2.批量定义变量
```
    class Program
    {
        static void Main(string[] args)
        {
		string message1,message2,message3;//批量定义变量
		message1 = Console.ReadLine();//接收输入的值赋值给变量
		message1 = message2 = message3;//批量赋值
            	Console.WriteLine(message1,message2,message3);//批量输出
            	Console.ReadKey();//输出停留，等待按键结束
        }
    }
```
3.格式化输出
```
class Program
    {
        static void Main(string[] args)
        {
            string name;
            Console.Write("你的名字是：");//删除WriteLine的Line可以让输入光标在后面
            name = Console.ReadLine();//接收输入
            Console.WriteLine("你的名字是" + name);//连接字符输出
            Console.WriteLine("你的名字是{0}",name);//占位符输出
            Console.ReadKey();
        }
    }
```
4. 数据类型-基本类型
	1. 8种、整数类型
		1. int-32bit
		2. long-64bit
	2. 2种、用于科学计算的浮点类型
		1. float-32bit-有效数字7位
		2. double-64bit-有效数字+15~-16位
	3. 1种、金融计算浮点类型
		1. decimal-128bit-用于金融计算货币
	4. 1种、布尔类型
		1. bool isCool = true / false
	5. 1种、字符类型
		1. char ch = '1';//char只能输入一个字符并使用单引号
		2. 关于转义符 回车\n, TAB\t, \\\, \', \a
		3. string 字符串可以嵌入转义符 @ 用于输出路径
			1. 由于string字符的不可变性使用str.ToUpper();函数需要重新赋值给str 如str1 = str1.ToUpper();
				```
				using System;
				using System.Collections.Generic;
				using System.Linq;
				using System.Text;
				using System.Diagnostics;//加入计时器模块

				namespace ConsoleApplication2
				{
					class Program
					{
						static void Main(string[] args)
						{
							Stopwatch 计时器 = new Stopwatch();
							计时器.Start();
							/StringBuilder sb = new StringBuilder();
							//for (int i = 0; i < 10000; i++)
							//{
							//    sb.Append(i.ToString());
							//}效率高
							string str = string.Empty;//空的
							for (int i = 0; i < 10000; i++)
							{
								str += i.ToString();
							}//转换字符相加效率低

							计时器.Stop();
							Console.WriteLine(计时器.ElapsedMilliseconds);
							Console.ReadKey();
						}
					}
				}
			```
	6. 字面值、根据输入的类型自动转换INT/DOUBLE
		1. 指数型写法 字面量 doubel num = 2E10 //2的10次方
		2. 十六进制 字面量 num = Oxff //255
5. 复合类型
	1. null与Empty不同-null表示根本没有出现过或者不存在，没有开辟内存空间；null为数据库准备的类型 int? number = null;
	2. var隐式类型   如var i = 1;//可以是整型也可以是INT类型
6. 类型转换
	1. 显示、从高向低、checked
		1. int a;  long b; a = (int)b;
		2. checked(//检查转换类型是否溢出)
	2. 隐式、从低向高、
	3. 专门的转换函数
		1. int.Parse()用于输入字符转换INT相加输出
			```
			var str1 = Console.ReadLine();
            var str2 = Console.ReadLine();
            int a1 = int.Parse(str1);
            int a2 = int.Parse(str2);
            Console.WriteLine(a1 + a2);
            Console.ReadKey();
			```
		2. TryParse//解析转换是否成功，并输出错误信息
			```
			var str1 = Console.ReadLine();
            var str2 = Console.ReadLine();
            int a1;
            if (int.TryParse(str1, out a1))
            {
                Console.WriteLine(a1);
            }
            else
            { 
                Console.WriteLine("解析失败"); 
			```
		3. ToString 转换成string类型
		4. System.Convert()//查说明