
## const 和 \*
1. const表示常量，\*是指针
2. 以从右向左的方式解读
	* ***const int * a*** 表示a是int指针，const修饰这个指针，则为常量指针
	* **int \*const a** 表示const修饰a是一个常量对象，这个常量对象是int\*类型
3. 顶层const表示常量指针，底层const表示指针对象是常量


## String
1. +法运算 stirng s = “a” + “b" + string("a")等同于 s = ("a" + "b") + string("a")
	而("a" + " b") 是非法的，所以该用法错误

## 类型转换
1. static_cast
	不能对底层const转换，对编译器显式的进行类型转换
2. dynamic_cast
	
3. const_cast
	对底层const进行转换，可以将const变量转换为非const变量。需要保证源头的变量是非常量的，不然对变量进行改变是ub行为
4. reinterpret_cast
	直接做类型的强转，但是只能对指针进行转换，同时也无法对底层const进行转换

## 迭代器

## Assert
	位于头文件<cassert>中根据宏指令NDEBUG而不生效可以在编译指令加入NDEBUG宏指令

## 迭代器
> 除了容器里面定义的迭代器之外，还有额外的4个迭代器
1. 插入迭代器(insert iterator)：与容器绑定，对其赋值之后会将值插入容器中，分为3种迭代器
	-  back_inserter，调用push_back
	- front_inserter，调用push_front
	- inserter，接受两个参数，第二个参数是容器迭代器，会插入在对应迭代器的位置之前
1. 流迭代器(stream iterator)：与流绑定，在对迭代器操作的时候，实际上是会对绑定的输入输出流进行写入或者读取
1. 反向迭代器(reverse iterator)：相当于正常迭代器的方向操作
2. 移动迭代器(move iterator)：


