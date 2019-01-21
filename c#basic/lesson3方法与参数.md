# lesson 3
## 方法和参数
1. 结构
	1. System（命名空间）.Console（类）.WriteLine（方法）("（参数）");
	2. 命名空间用于跨模块使用类与方法的功能（如using 或者在类前面加上命名空间全称即namespace）
2. 调用
	1. 动态可以调用动态void、静态static
	2. 静态只能调用静态
3. 返回
	1. 单一返回一个值returm，不能用于void函数
4. 参数
	1. 列表参数(List<\int> list)
	2. 形参与实参
	3. 值类型与引用类型ref、out
		1. 	在不使用ref时，在两方法间传递参数是一个值拷贝开辟新内存空间，一个方法内参数变化不影响其他方法的参数
		2. 	使用ref int a,则两方法参数指向同一内存地址，同时变化
		3. list 引用类型(引用内存地址)，string int double bool char基本类型需要加ref
		4. out
5. 重载： 指相同方法名不同参数类型的多个方法
6. 泛型：static vodi func<T>(){}在方法后面加入<T>可以设置为重载模版，后续使用为static vodi func<\string>(){}
7. 可变参数params必须是最后一个形参
8. 递归static long FileOrDirCount(string path)
	1. 统计file的个数
		1.long count = 0;
		1. var files = Directory.GetFiles(path);
		2. count += files.length
	2. 统计directory的个数
		1. var dirs = Directory.GetDirectorise(path);
		2. foreach(var dir in dirs)
		3. {count += FileOrDirCount(dir);}
9. 捕获异常 try{}catch(){throw}