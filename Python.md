# The Zen of Python —— by Tim Peters

参考：https://www.runoob.com/python3/python3-tutorial.html

> Beautiful is better than ugly.
> Explicit is better than implicit.
> Simple is better than complex.
> Complex is better than complicated.
> Flat is better than nested.
> Sparse is better than dense.
> Readability counts.
> Special cases aren't special enough to break the rules.
> Although practicality beats purity.
> Errors should never pass silently.
> Unless explicitly silenced.
> In the face of ambiguity, refuse the temptation to guess.
> There should be one-- and preferably only one --obvious way to do it.
> Although that way may not be obvious at first unless you're Dutch.
> Now is better than never.
> Although never is often better than *right* now.
> If the implementation is hard to explain, it's a bad idea.
> If the implementation is easy to explain, it may be a good idea.
> Namespaces are one honking great idea -- let's do more of those!

---



## 变量和简单数据类型

### 字符串

> 在python中，引号括起来的都是字符串 非常的灵活



> rstrip()删除字符串末尾空白
> lstrip()删除字符串开头空白
> strip()删除字符串两端空白

---



### 数字

> Python使用两个**表示乘方运算
>
> eg: 3 ** 2 = 9



> 使用函数str()可以将非字符串值表示为字符串

---

### 注释

> # or 三个“”

---





## 列表

>  []表示 ,用来分隔元素

> append在列表末加上新的元素
>
> array.append(‘newElement’)

> insert() 函数用于将指定对象插入列表的指定位置。

> del() 可删除任何位置处的列表元素
>
> pop() 弹出元素



> remove() 删除值 
>
> PS：只能删除第一个指定的值 删除所有指定的值需要循环



> sort()永久性修改列表元素的排列顺序 按字母排序
>
> sort(reverse = True) 字母倒序

> sorted() 非永久性

> reverse 永久性 倒序打印

> len() 快速获悉列表的长度

> split() 切片

> list() 用于将元组或字符串转换为列表

> 缩进表示所属关系

---



> range(x,y) 打印 x —— y-1
>
> 使用range还可以指定步长 range(x,y,z) 步长为z

> min(); max(); sum() 对数字列表进行简单的计算

---



### 切片

> [x:y] (x + 1) —— y个元素 
>
> 没有起始索引 将从列表开头开始提取
>
> 没有终止索引 将一直提取到结尾

---



### 元组

> Python将不能修改的值称为不可变的，
>
> 而不可变的列表被称为元组

---





## if语句

> ### 条件测试



> 使用 and 检查多个条件
>
> 使用 or  检查多个条件
>
> 使用 （not) in 检查特定的值是否在列表

---



### if-elif-else结构

> 与C类似

---





## 字典

> str 访问字典中的值

---





## 用户输入＆while循环

### input()

> 函数int() 将输入视为数值 可以将数字的字符串表示为数值表示	

> break: 以while True 打头的循环将不断运行运行 直到遇到break语句

> continue 忽略余下的代码 返回到循环的开头

---



### while

> 使用while循环删除列表中的值

---





## 函数

### 创建

> 编写函数时，可给每个形参指定**默认值**

> return is good

> 形参名 ***name** 中的星号让Python创建一个名为那么的空元组并将收到的所有制都封装到这个元组中。

> 函数是一种拥有无限键值对的字典。不同的键可以有同一输出，但同一输出不能有不同的值

> **x创建了字典x， *x创建了元组x
> 之所以创建的是元组而不是列表，是因为元组
> 不可修改且占用资源少，更加安全高效

> 在函数定义中，如果有默认参数，Python 要求将这些默认参数放在参数列表的末尾。这是因为在调用函数时，Python 会按照位置顺序将参数传递给函数。如果默认参数放在了非默认参数之前，那么在调用函数时，解释器可能会无法确定参数的传递顺序，从而导致错误。

---



### 导入

> import 导入函数
> form x~1~ inport x~2~ 导入模块中的特定函数

> （form x~1~） inport x~2~ as x~3~ 
>
> 使用as给模块指定别名

> form x~1~ inport *
>
> 导入模块中的所有函数

---





## 类

### 创建

> 首字母大写的名称指的是类
>
> 类中的函数称为方法： 开头和末尾都要有__

---



### 继承

> ​	如果你要编写的类是另一个类的现成类的特殊版本，可使用**继承**
>
> ​	一个类**继承**另一个类时，它将自动活得另一个类的所有属性和方法；原有的类称为**父类**，而新的类称为**子类**

> ​	super()是一个特殊函数，磅数Python将父类和子类关联起来 父类也成为超类

---





## 文件和异常

### 读取

> ​	函数open()接受一个参数：要打开的文件的名称



> ​	调用open可使用两个实参，第一个实参是文件名称，第二个实参表示以什么模式打开

> ​	如果指定的文件已经存在，以写入模式打开，Python将在返回文件对象钱清空该文件

---



### 异常

> ​	使用try—except代码块

> ​	pass 让Python什么都不做

---



### 存储

> ​	使用模块json来存储数据	<u>JSON(JaveScript Object Notation)格式最初是为JaveScript开发的，但随后成了一种常见格式，被包括Python在内的众多语言采用</u>

---





## 测试代码

### 断言

> ​	Python assert 用于判断一个表达式，在表达式条件为false的时候触发异常。

> ​	断言可以在条件不满足程序运行的情况下返回错误，而不必等待程序运行后出现崩溃的情况，例如我们的代码只能在 Linux 系统下运行，可以先判断当前系统是否符合条件。

> |           方法           |        用途        |
> | :----------------------: | :----------------: |
> |    assertEqual(a, b)     |     核实a == b     |
> |   assertNotEqual(a, b)   |     核实a != b     |
> |      assertTrue(x)       |    核实x为True     |
> |      assertFalse(x)      |    核实x为False    |
> |   assertIn(item, list)   |  核实item在list中  |
> | assertNotIN（item, list) | 核实item不在list中 |
>

---



### 测试

> `unittest.main()` 是在运行测试模块时调用的。它告诉 Python 解释器运行 `unittest` 模块中的测试。当你运行这个脚本时，它会查找定义的测试类 `TestAnonySurey` 中的测试方法并执行它们。

---



### 方法setUp()

> ​	unittest.Testcase类包含方法setUp(),让我们只需创建这些对象一次，并在各个测试方法中使用它们。如果你在TestCase类中包含了方法setUo()，Python将先运行它，再运行各个以test_打头的方法。这样，在你编写的每个测试方法中都可使用在方法setUp()中创建的对象了
>
> PS：每次在运行以test_打头的方法时，set_Up()都会运行一次，而不是只在测试开始时运行一次。

---









# Web应用程序



## Django入门

> 序言：当今的网站实际上都是富应用程序(rich application),就像成熟的桌面应用程序一样。

> Django是一个**Web框架** —— 一套用于帮助开发交互式网站的工具。

---







# Nowcoder

## input()

### 保留小数

1. 使用字符串格式化：

```python
pythonCopy code# 读入数据
input_data = float(input("请输入数据："))

# 输出数据并保留两位小数
print("{:.2f}".format(input_data))
```

2. 使用 `round()` 函数：

```python
pythonCopy code# 读入数据
input_data = float(input("请输入数据："))

# 输出数据并保留两位小数
rounded_data = round(input_data, 2)
print("保留两位小数输出：", rounded_data)
```

这两种方法都可以确保输出的数据保留两位小数。

---



### **全部大写 全部小写 首字母大写**

```python
user_input = input()
uppercase_string = user_input.upper()
lowercase_string = user_input.lower()
titlecase_string = user_input.capitalize()
print("全大写形式:", uppercase_string)
print("全小写形式:", lowercase_string)
print("首字母大写形式:", titlecase_string)
```

PS ：如果遇到有空格的字符串 还需要将每一段字符的首字母转换成大写 需要使用  **title()**

---



### 去除空白

```python
user_input = input("请输入一个字符串: ")

# 去除字符串两侧的空白
trimmed_string = user_input.strip()

# 去除字符串左侧的空白
left_trimmed_string = user_input.lstrip()

# 去除字符串右侧的空白
right_trimmed_string = user_input.rstrip()

print("去除两侧空白后的字符串:", trimmed_string)
print("去除左侧空白后的字符串:", left_trimmed_string)
print("去除右侧空白后的字符串:", right_trimmed_string)

```

---



### 实现截取字符串

```python
user_input = input("请输入一个字符串: ")

# 使用字符串切片截取前十个字符
first_ten_characters = user_input[:10]

print("截取的前十个字符:", first_ten_characters)
					
```

---



### 遍历列表 并且替换

```python
offer_list = ["Allen", "Tom"]

# 打印面试通过的消息
for name in offer_list:
    print(f"{name}, you have passed our interview and will soon become a member of our company.")

# 打印欢迎消息并替换'Tom'为'Andy'
for name in offer_list:
    if name == "Tom":
        offer_list[offer_list.index("Tom")] = "Andy"
    else:
        print(f"{name}, welcome to join us!")
print("Andy, welcome to join us!")

```

---



