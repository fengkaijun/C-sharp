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
			string message1,message2,message3;//批量定义变量
			message1 = Console.ReadLine();//接收输入的值赋值给变量
			message1 = message2 = message3;//批量赋值
            Console.WriteLine(message1,message2,message3);//批量输出
            Console.ReadKey();//输出停留，等待按键结束
        }
    }
}
```

