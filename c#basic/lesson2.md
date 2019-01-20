# lesson 2
## 运算符
1. 一元运算符
	1. \+加号  -减号 
2. 二元运算符
	1. *乘号、/除号、%求余数
		1. %求余数（用于比如分组2人一组）
	2. +=累加、-=累减、++递加、--递减、%=余等于、/=自除
	3. 注意：结合性和优先级，（）、
	4. 字符串+、
	4. 浮点数运算
	4. 常量const
3. 三元运算符
## 三大结构
1. 顺序结构
2. 分支结构
	1. if(){} else
	2. switch(){} default; case: break;
	3. bool exp = 1 > 2(比较操作符<=， >=， !=， ==;逻辑运算符 或||， 与&&，求反！优先级高)
	4. bool变量用is开头命名
	5. 三元操作符 a>b?a:b
	6. 空结合运算符  a??b
		```
		string fileName = null;
		fileName = fileName??"default.txt";
		Console.WriteLine(fileName);
		```
	7.  按位运算符
3. 循环结构