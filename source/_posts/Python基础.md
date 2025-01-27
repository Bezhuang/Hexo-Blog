---
title: Python 基础知识总结
date: 2020-10-11
tags: []
categories: 待分类
references:
  - title: Python教程
    url: https://www.liaoxuefeng.com/wiki/1016959663602400
  - title: Python 基础教程
    url: https://www.bilibili.com/video/BV1hW41197sB
---

> Python 是由 Guido van Rossum 在八十年代末和九十年代初，在荷兰国家数学和计算机科学研究所设计的一个高层次的结合了解释性、编译性、互动性和面向对象的脚本语言。Python 的设计具有很强的可读性，相比其他语言经常使用英文关键字，其他语言的一些标点符号，它具有比其他语言更有特色语法结构。以下为我在学习和实战练习过程中所做的笔记，可供参考。

<!--more-->

### 计算机的使用方式

- Interface 交互界面
- TUI（文本交互界面）和 GUI（图形化交互界面）
- windows 的命令行
- 环境变量（environment variable）
  - path 环境变量

### 进制

- 十进制（最常用的进制）
- 二进制（计算机底层使用的进制）
  - bit 是计算机中的最小的单位
  - byte 是我们最小的可操作的单位
- 八进制（一般不用）
- 十六进制
- 我们在查看二进制数据时，一般会以十六进制的形式显示

### 文本文件和字符集

- 文本分成两种，一种叫做纯文本，还有一种叫做富文本
- 编码；解码；字符集
- 常见的字符集：ASCII；ISO-8859-1；GB2312；Unicode，最常用的就是 UTF-8
- 乱码

### 计算机语言

- 机器语言
- 符号语言（汇编）
- 高级语言
- 编译型语言和解释型语言

### 基本语法概念

- 表达式
- 语句
- 程序（program）
- 函数（function）
- 严格区分大小写
- 每一行语句不要过长（规范中建议每行不要超过 80 个字符）
- 多行编写时语句后边以\结尾
- 注释要求简单明了，一般习惯上#后边会跟着一个空格

### 字面量、变量和标识符

- 在程序中可以直接使用字面量
- 变量（variable）变量可以用来保存字面量

### 数据类型

- 数据类型指的就是变量的值得类型，也就是可以为变量赋哪些值
- 数值：整数、浮点数、复数
- 整型：`0b`（二进制）`0x`（十六进制）`0o`（八进制）
- 字符串：`\t` 缩进 `\n` 换行 `\uxxxx`表示 unicode 编码
- 格式化字符串：`%s` 任意字符 `%f` 浮点数占位符 `%d` 整数占位符
- 布尔值：`True` `False`
- 空值：`None`
- 类型检查：`type()`

### 对象（object）

- Python 是一门面向对象的语言
- 对象就是内存中专门用来存储指定数据的一块区域
- 数值、字符串、布尔值、None 都是对象
- 每个对象中都要保存三种数据
  1. id（标识）：唯一性，`id()`函数，解析器生成，不能改变
  2. type（类型）：`type()`函数，强类型—创建类型后便不能修改
  3. value（值）：可变对象、不可变对象

### 变量和对象

- 对象并没有直接存储到变量中，在 Python 中变量更像是给对象起了一个别名
- 变量中存储的不是对象的值，而是对象的 id，当我们使用变量时，实际上就是在通过对象 id 在查找对象
- 变量中保存的对象，只有在为变量重新赋值时才会改变
- 变量和变量之间是相互独立的，修改一个变量不会影响另一个变量

### 类型转换

- 类型转换是将一个类型的对象转换为其他对象
- `int()`、`float()`、`str()`、`bool()`
- 类型转换不是改变对象本身的类型，而是根据当前对象的值创建一个新对象

### 运算符(操作符)

- 运算符可以对一个值或多个值进行运算或各种操作
- 运算符的分类：
  1. 算术运算符：`//`整除、`%余`数
  2. 赋值运算符
  3. 比较运算符（关系运算符）：`==`等于、`!=`不等于、字符比较unicode 编码、`is (is not)`比较 id
  4. 逻辑运算符：`not`、`and`、`or`
  5. 条件运算符（三元运算符）：`a if a>b else b`

### 流程控制语句

- Python 代码在执行时是按照自上向下顺序执行的
- 通过流程控制语句，可以改变程序的执行顺序，也可以让指定的程序反复执行多次
- 流程控制语句分成两大类：条件判断语句，循环语句

### 条件判断语句（if 语句）

- if、elif、else
- try、except

### 循环语句（while、for 语句）

- while、else、for
- break、continue、pass（占位）

### 循环嵌套

- 外层循环控制图形的高度
- 内层循环控制图形的宽度
- `print(x, end=" "）`不换行输出

### 序列（sequence）

- 序列是 Python 中最基本的一种数据结构
- 数据结构指计算机中数据存储的方式
- 序列用于保存一组有序的数据，所有的数据在序列当中都有一个唯一的位置（索引），并且序列中的数据会按照添加的顺序来分配索引
- 序列的分类：
  1. 可变序列（序列中的元素可以改变）：
     - 列表（list）
  2. 不可变序列（序列中的元素不能改变）：
     - 字符串（str）
     - 元组（tuple）

### 列表（list）

- 列表是 Python 中的一个对象
- 对象（object）就是内存中专门用来存储数据的一块区域
- 之前我们学习的对象，像数值，它只能保存一个单一的数据
- 列表中可以保存多个有序的数据
- 列表是用来存储对象的对象
- `len()`，所取长度 = 最后一位索引+1
- 列表`[0:8:2]`，`起始：结束：间隔`，包含开始不包含结束，间隔若为负数则从后往前取
- `min()`，`max()`，`in`，`not in`
- `xxx.index('n',0,8)` 获取指定元素在列表中的位置，`xxx.count() `统计元素在列表中出现次数
- `xxx.append(x) `插入元素到末尾，`s.insert('x', 2) `插入元素+插入索引位置，`x.extend([x,y,z]) `插入列表
- `del [1:2] = x.remove(1)`，`xxx[0:2] = ['x','y'] `替换元素，`x.pop(2) `删除索引位置的元素并返回此元素
- `x.reverse() `反转，`x.sort() `排序，默认升序，`x.sort(reverse=True) `为降序
- `for x in xlist` 遍历序列，`range()` 函数生成自然数列

### 元组（tuple）

- 元组是不可变的序列 `tuple = (1, 2, 3, 4, 5)`
- 当元组不是空元组时，括号可以省略
- 元组的解包 `a, b, *c = tuple`，c 为`[3, 4, 5]`

### 可变对象

- 每个对象中都保存了三个数据：
  - id（标识）
  - type（类型）
  - value（值）
- 列表就是一个可变对象
- 一般只有在为变量赋值时才是修改变量，其余的都是修改对象
- `==`、`!= `比较对象的值，`is`、`is not` 比较对象的 `id`

### 字典（dict）

- 字典属于一种新的数据结构，称为映射（mapping）
- 字典的作用和列表类似，都是用来存储对象的容器
- 列表存储数据的性能很好，但是查询数据的性能的很差
- 在字典中每一个元素都有一个唯一的名字，通过这个唯一的名字可以快速的查找到指定的元素
- 在查询元素时，字典的效率是非常快的
- 在字典中可以保存多个对象，每个对象都会有一个唯一的名字
  - 这个唯一的名字，我们称其为键（key），键可以是任意的不可变对象
  - 通过 key 可以快速的查询 value
  - 这个对象，我们称其为值（value），值可以是任意对象
  - 所以字典，我们也称为叫做键值对（key-value）结构
  - 每个字典中都可以有多个键值对，而每一个键值对我们称其为一项（item）
- `{key : value, key : value}`、`d = dict(k1 = v1 , k2 = v2 , k3 = v3)`、`d = dict[ (k1 , v1) , (k2 , v2) , (k3 , v3) ]`
- `d[key]`、`d.get(key , 默认值)` 如不存在 key 则返回默认值、`d[key] = value`
- `in`、`not in` 检查键 key、
- `.setdefault(key[ , default ]) `如果 key 存在，返回 key 的值，如果 key 不存在，添加并返回默认值
- `.update([other])` 将其他字典中的 key-value 添加到当前字典，若 key 重复则替换
- `.popiterm()` 默认删除最后一个键值对，返回的是元组`(key,value)`，`pop(key , 默认值)`返回 value 或默认值
- `.clear()`清空、`.copy()`用于对字典进行浅复制（复制后的对象和原对象相互独立）（不复制可变对象）
- `.keys()`会返回字典的所有 key，`.values()`返回字典的所有 value，`.items()`返回字典中所有项（双值子序列）、`for k, v in d.items(): print(k , v)`

### 集合（set）

- 集合和列表非常相似
- 不同点：
  1. 集合中只能存储不可变对象
  2. 集合中存储的对象是无序（不是按照元素的插入顺序保存）
  3. 集合中不能出现重复的元素
- `set()`、`{}`、`s = set('Hello') → {'H' , 'e' , 'l' , 'o'}`
- `.add()`向集合中添加元素、`.update()`将集合/元组/字典(key)中元素添加至集合中
- `.pop()`随机删除并返回元素、`.remove()`删除指定元素、`copy() `浅复制
- `s & s2` 交集运算，`s | s2` 并集运算，`s - s2 `差集运算，`s ^ s2 `亦或运算

### 函数（function）

- 函数也是一个对象
- 对象是内存中专门用来存储数据的一块区域
- 函数可以用来保存一些可执行的代码，并且可以在需要时，对这些语句进行多次的调用
- 创建函数：
  - `def 函数名([形参 1,形参 2,...形参 n])：代码块`
  - 函数名必须要符号标识符的规范（可以包含字母、数字、下划线、但是不能以数字开头）
  - 函数中保存的代码不会立即执行，需要调用函数代码才会执行
  - 调用函数：`函数对象()`
  - 定义函数一般都是要实现某种功能的

### 函数的参数

- 在定义函数时，可以在函数名后的()中定义数量不等的形参，多个形参之间使用,隔开
- 形参（形式参数），定义形参就相当于在函数内部声明了变量，但是并不赋值
  - 定义形参时，可以指定默认值
- 实参（实际参数）
  - 如果函数定义时指定了形参，那么在调用函数时也必须传递实参，实参将会赋值给对应的形参
  - 有几个形参就得传几个实参
- 实参的传递方式
  - 位置参数
  - 关键字参数
  - 混合使用时，必须把位置参数放前面
- 实参可以传递任意类型的对象
- 在函数中对形参进行重新赋值不会影响其他变量
- 如果形参执行的是一个对象，那么通过形参修改对象会影响到所有指向该对象的变量
- 定义函数形参前加 `*`，那么这个形参会获取到所有实参（将所有实参保留到元组），使用时遍历元组
- 可变参数不是必须写最后，但带`*`后的所有参数必须用关键字参数传递
- `**`形参可以接收其他的关键字参数，并将它们保存在字典中
- 传递实参前加`*`可以将序列中元素依次传递（参数解包），`**`则对字典解包
- `return` 返回值，可返回任意对象，return 一旦指向函数自动结束

### 作用域与命名空间

- `help()`
- 文档字符串就是定义函数的说明，在函数第一行写一个字符串就是文档字符串
- `def() -> str`：表示返回值是字符串，同样为文档字符串
- 作用域（scope）指的是变量生效的区域
- 全局作用域与函数作用域
- `global a` 声明在函数内部使用的 a 是全局变量，此时再修改 a 就是修改全局 a
- 命名空间（namespace）指的是变量存储的位置，实际是一个储存变量的字典
- 每一个 scope 都有对应的 namespace
- 全局命名空间用来保存全局变量，函数命名空间用来保存函数的变量
- `locals()`用来获取当前作用域的命名空间
- `scope['c'] = ...`向字典中添加 key-value 等于在当前作用域中创建了一个变量
- `global() `在任意位置获取全局命名空间

### 函数式编程

- 递归式函数（自己调用自己）
  1. 基线条件（可被分成的最小问题，满足即停止指向）
  2. 递归条件（将问题继续分解的条件）
- 在 Python 中，函数是一等对象
- 一等对象一般都会具有如下特点：
  1. 对象是在运行时创建的
  2. 能赋值给变量或作为数据结构中的元素
  3. 能作为参数传递
  4. 能作为返回值返回
- 高阶函数（接收函数作为参数或将函数作为返回值的函数）
  - `filter() `从序列中过滤出符合条件的元素并保存到新的序列（可迭代结构）
- 匿名函数
  - lambda 函数表达式（` lambda 参数列表: 返回值`）`(lambda a,b : a+b)`
  - 匿名函数也可以直接赋值给一个变量
  - `map()` 函数可以对可跌倒对象中的元素修改并添加到新变量并返回
  - 匿名函数一般作为参数使用
- `sort()` 对列表中的元素进行排列，也可以接收关键字参数（key=...）比较函数返回值
- `sorted()`可对任意序列排序且不影响原来的对象，而是返回一个新对象
- 闭包是将函数作为返回值的函数，可以创建只有当前函数能访问的变量
- 装饰器
  - 在不修改原有函数的情况下扩展函数的功能  
    `def funtion(*args ,**kwargs)`
    `result = old(*args ,**kwargs)`
  - @引用指定装饰器
  - 一个函数指定多个装饰器时，函数安装从内向外引用装饰器

### 对象

- 对象是内存中专门用来存储数据的一块区域。
- 对象中可以存放各种数据（比如：数字、布尔值、代码）
- 对象由三部分组成：
  1. 对象的标识（id）
  2. 对象的类型（type）
  3. 对象的值（value）

### 面向对象（oop）

- Python 是一门面向对象的编程语言
- 所谓的面向对象的语言，简单理解就是语言中的所有操作都是通过对象来进行的
- 面向过程的编程的语言
  - 面向过程指将我们的程序的逻辑分解为一个一个的步骤，通过对每个步骤的抽象，来完成程序
  - 面向过程的编程思想将一个功能分解为一个一个小的步骤，我们通过完成一个一个的小的步骤来完成一个程序
  - 这种编程方式，符合我们人类的思维，编写起来相对比较简单
  - 但是这种方式编写代码的往往只适用于一个功能，如果要在实现别的功能，即使功能相差极小，也往往要重新编写代码，所以它可复用性比较低，并且难于维护
- 面向对象的编程语言
  - 面向对象的编程语言，关注的是对象，而不关注过程
  - 对于面向对象的语言来说，一切都是对象
  - 面向对象的编程思想，将所有的功能统一保存到对应的对象中，要使用某个功能，直接找到对应的对象即可
  - 这种方式编写的代码，比较容易阅读，并且比较易于维护，容易复用。
  - 但是这种方式编写，不太符合常规的思维，编写起来稍微麻烦一点
  - 简单归纳一下，面向对象的思想
    1. 找对象
    2. 搞对象

### 类(class)

- 我们目前所学习的对象都是 Python 内置的对象
- 但是内置对象并不能满足所有的需求，所以我们在开发中经常需要自定义一些对象
- 类，简单理解它就相当于一个图纸。在程序中我们需要根据类来创建对象
- 类就是对象的图纸
- 我们也称对象是类的实例（instance）
- 如果多个对象是通过一个类创建的，我们称这些对象是一类对象
- 像 `int()`, ` float() `, `bool()`, ` str()`, ` list()`,  `dict()` .... 这些都是类
- `a = int(10)` # 创建一个 `int` 类的实例 等价于 ` a= 10`
- 我们自定义的类都需要使用大写字母开头，使用大驼峰命名法（帕斯卡命名法）来对类命名
- 类也是一个对象
- 类就是一个用来创建对象的对象
- 类是 type 类型的对象，定义类实际上就是定义了一个 type 类型的对象
- `isinstance()`用来检查一个对象是否是一个类的实例

### 使用类创建对象的流程

1. 创建一个变量
2. 在内存中创建一个新对象
3. 将对象的 id 赋值给变量

- 向对象中添加变量，对象中的变量称为属性
- 语法：`对象.属性名 = 属性值`

### 类的定义

- 类和对象都是对现实生活中的事物或程序中的内容的抽象
- 实际上所有的事物都由两部分构成：
  1. 数据（属性）
  2. 行为（方法）
- 在类中定义的函数称为方法，方法可通过该类的所有实例来访问
- 在类的代码块中，我们可以定义变量和函数
  - 变量会成为该类实例的公共属性，所有的该类实例都可以通过 `对象.属性名` 的形式访问
  - 函数会成为该类实例的公共方法，所有该类实例都可以通过 `对象.方法名()` 的形式调用方法
  - 注意：方法调用时，第一个参数由解析器自动传递，所以定义方法时，至少要定义一个形参
- 实例为什么能访问到类中的属性和方法
  - 类中定义的属性和方法都是公共的，任何该类实例都可以访问
- 属性和方法查找的流程
  - 当我们调用一个对象的属性时，解析器会先在当前对象中寻找是否含有该属性
  - 如果有，则直接返回当前的对象的属性值，如果没有，则去当前对象的类对象中去寻找，如果有则返回类对象的属性值，如果类对象中依然没有，则报错
- 类对象和实例对象中都可以保存属性（方法）
  - 如果这个属性（方法）是所有的实例共享的，则应该将其保存到类对象中
  - 如果这个属性（方法）是某个实例独有，则应该保存到实例对象中
- 一般情况下，属性保存到实例对象中，而方法需要保存到类对象中
- `def method(self):`

### 类的特殊方法

- 在类中可以定义一些特殊方法（魔术方法）
- 特殊方法都是以`__`开头，`__`结尾的方法，且不手动调用
- `def __init__(self):`
- 创建对象的流程（ `p1 = Person()`的运行流程 ）
  1. 创建一个变量
  2. 在内存中创建一个新对象
  3. `__init__(self)`方法执行
  4. 将对象的 id 赋值给变量
- `init `会在对象创建以后立刻执行
- `init `可以用来向新创建的对象中初始化属性`（self.name）`
- 直接通过 对象.属性 的方式可以来修改属性的值，但这样对象中的属性可以随意修改

### 类的基本结构

- class 类名([父类]) :
  公共的属性...
  `def __init__(self,...):`(对象的初始化方法)
  ...
  `def method_1(self,...):`(其他的方法)
  ...
  `def method_2(self,...):`
  ...

### 封装

- 封装是面向对象的三大特性之一
- 封装指的是隐藏对象中一些不希望被外部所访问到的属性或方法
- `getter` 和 `setter` 方法使外部可以访问到属性
  - `getter` 获取对象中的指定属性（`get_属性名`）(`return self.name`）
  - `setter` 用来设置对象中的指定属性（`set_属性名`）
  - 如果希望属性只读，去除 `setter` 方法
  - 如果不希望属性被外部访问，则去除 `getter` 方法
  - 使用 `setter` 方法设置属性，可以增加数据的验证，确保数据的值是正确的
- 使用封装确实增加了类的定义的复杂程度，但是它也确保了数据的安全性

### 隐藏类中的属性

- 可以为对象的属性使用双下划线开头，`__xxx`
  - 双下划线开头的属性，是对象的隐藏属性，隐藏属性只能在类的内部访问，无法通过对象访问
  - 其实隐藏属性只是 Python 自动将属性名改名为`_类名__属性名`
- 一般我们会将私有属性（不希望被外部访问的属性）以`_`开头，没有特殊需要不要修改私有属性

### property 装饰器

- property 装饰器，用来将一个 get 方法，转换为对象的属性
- 添加为`@property`装饰器以后，我们就可以像调用属性一样使用 `get`方法
- 使用 property 装饰的方法，必须和属性名是一样的
- setter 方法的装饰器：`@属性名.setter`

### 继承

- 继承是面向对象的三大特性之一
- 继承其他类中的属性和方法
- 在定义类时，可以在类名后的括号中指定当前类的父类（超类）
- 子类（衍生类）可以直接继承父类中的所有的属性和方法
- 我们经常需要通过继承来对一个类进行扩展
- 在创建类时，如果省略了父类，则默认父类为 object，object 是所有类的父类，即所有类都继承自 object
- `issubclass()` 检查一个类是否是另一个类的子类
- `isinstance()` 检查一个对象是否是一个类的实例，如果这个类是这个对象的父类，也会返回 true，所有对象都是 object 的实例

### 方法的重写（override）

- 如果在子类中如果有和父类同名的方法，则通过子类实例去调用方法时，会调用子类的方法为不是父类的方法
- 当我们调用一个对象的方法时，会优先去当前对象中寻找是否具有该方法
  - 如果有则直接调用，如果没有则去当前对象的父类中寻找
  - 如果没有，则去父类的父类中寻找，以此类推到 object，如还没则报错
- 父类中所有方法（包括特殊方法）都会被子类继承，也可以重写特殊方法
- `super()` 可以用来获取当前类的父类，并且通过 `super() `返回对象调用父类方法时，不需要传递 `self`

### 多重继承

- 在 Python 中是支持多重继承的，也就是我们可以为一个类同时指定多个父类
- 可以在类名的 `() `中添加多个类，来实现多重继承
- 多重继承，会使子类同时拥有多个父类，并且会获取到所有父类中的方法
- 在开发中没有特殊的情况，应该尽量避免使用多重继承，因为多重继承会让我们的代码过于复杂
- 如果多个父类中有同名的方法，则从前往后查找，即前边父类的方法会覆盖后边父类的方法
- 类名，`__bases__`这个属性可以用来获取当前类的所有父类
- `print(C.__bases__)` `(<class '__main__.B'>,)`
- ` print(B.__bases__)``(<class 'object'>,) `

### 多态

- 多态是面向对象的三大特征之一
- 一个对象可以以不同的形态去呈现，即多态
- 如函数违反多态，只适用于一种类型的对象，无法处理其他类型对象，则函数适应性会变差
- 多态的描述：鸭子类型
  - 如果一个东西，走路像鸭子，叫声像鸭子，那么它就是鸭子
- 对象通过 `len()` 来获取长度，是因为对象中有`__len__`特殊方法
- 只要对象中具有`__len__`特殊方法，就可以通过 `len() `来获取长度

### 面向对象的三大特征的总结

- 封装
  - 确保对象中的数据安全
- 继承
  - 保证了对象的可扩展性
- 多态
  - 保证了程序的灵活性

### 类中的属性和方法

- 类属性
  - 类属性，直接在类中定义的属性是类属性
  - 类属性可以通过类或类的实例访问到
  - 类属性只能通过类对象来修改，无法通过实例对象修改
- 实例属性和方法
  - 通过实例对象添加到属性属于实例属性
  - 在类中定义，以 `self `为第一个参数的方法是实例方法
  - 实例方法在调用时，Python 会调用对象作为 `self`传入
  - 实例方法可以通过实例和类去调用
    - 当通过实例调用时，会自动将当前调用对象作为 `self` 传入
    - 但通过类调用时，不会自动传递 `self`，此时我们必须手动传递 `self`
- 类方法
  - 在类内部使用 `@classmethod` 来修饰的方法属于类方法
  - 类方法的第一个参数是 `cls` ，也会被自动传递，`cls` 就是当前的类对象
- 实例方法
  - 实例方法的第一个参数是 `self`，类方法的第一个参数是 `cls`
  - 类方法可以通过类去调用，也可以通过实例调用，没有区别
- 静态方法
  - 在类中实用 `@staticmethod` 来修饰的方法属于静态方法
  - 静态方法不需要指定任何的默认参数，静态方法可以通过类和实例去调用
  - 静态方法基本是一个和当前类无关的方法，只是一个保存到当前类中的函数
  - 静态方法一般都是一些工具方法，和当前的需要无关

### 垃圾回收

- 就像我们生活中会产生垃圾一样，程序在运行过程当中也会产生垃圾
- 程序运行过程中产生的垃圾会影响到程序的运行的运行性能，所以这些垃圾必须被及时清理
- 在程序中没有被引用的对象就是垃圾，这种垃圾对象过多以后会影响到程序的运行的性能，所以我们必须进行及时的垃圾回收
- 所谓的垃圾回收就是将垃圾对象从内存中删除
- 在 Python 中有自动的垃圾回收机制，它会自动将这些没有被引用的对象删除，所以我们不用手动处理垃圾回收

### 特殊方法

- 特殊方法，也称为魔术方法
- 特殊方法都是使用`__`开头和结尾的
- 特殊方法一般不需要我们手动调用，需要在一些特殊情况下自动执行
- `__str__()`这个特殊方法会在尝试将对象转换为字符串的时候调用，它的作用可以用来指定对象转换为字符串的结果 （print 函数）
- `__repr__()`这个特殊方法会在对当前对象使用 repr()函数时调用，它的作用是指定对象在 “交互模式” 中直接输出的效果
- `object.__add__(self, other)`
- `object.__sub__(self, other)`
- `object.__mul__(self, other)`
- `object.__matmul__(self, other)`
- `object.__truediv__(self, other)`
- `object.__floordiv__(self, other)`
- `object.__mod__(self, other)`
- `object.__divmod__(self, other)`
- `object.__pow__(self, other[, modulo])`
- `object.__lshift__(self, other)`
- `object.__rshift__(self, other)`
- `object.__and__(self, other)`
- `object.__xor__(self, other)`
- `object.__or__(self, other)`
- `object.__lt__(self, other)` 小于 <
- `object.__le__(self, other)`小于等于 <=
- `object.__eq__(self, other)` 等于 ==
- `object.__ne__(self, other)` 不等于 !=
- `object.__gt__(self, other)` 大于 >
- `object.__ge__(self, other)` 大于等于 >=
- `__len__()`获取对象的长度
- `object.__bool__(self)`可以通过 bool 来指定对象转换为布尔值的情况
- `__gt__`会在对象做大于比较的时候调用，该方法的返回值将会作为比较的结果 他需要两个参数，一个 self 表示当前对象，other 表示和当前对象比较的对象：`self > other`

### 模块（module）

- 模块化，模块化指将一个完整的程序分解为一个一个小的模块，通过将模块组合，来搭建出一个完整的程序
  - 不采用模块化，统一将所有的代码编写到一个文件中
  - 采用模块化，将程序分别编写到多个文件中
- 模块化的优点：
  1. 方便开发
  2. 方便维护
  3. 模块可以复用
- 在 Python 中一个 `.py` 文件就是一个模块，要想创建模块，实际上就是创建一个 python 文件
- 注意：模块名要符号标识符的规范
- 在一个模块中引入外部模块
  1. `import 模块名` （模块名，就是 python 文件的名字，注意不要 py）
  2. `import 模块名 as 模块别名`
- 可以引入同一个模块多次，但是模块的实例只会创建一个
- import 可以在程序的任意位置调用，但是一般情况下，import 语句都会统一写在程序的开头
- 在每一个模块内部都有一个`__name__`属性，通过这个属性可以获取到模块的名字
- `__name__`属性值为`__main__`的模块是主模块，一个程序中只会有一个主模块
- 主模块就是我们直接通过 python 执行的模块
- 访问模块中的变量：`模块名.变量名`
- 只引入模块中的部分内容：`from 模块名 import 变量, 变量...`
- `from m import *` 引入到模块中所有内容，一般不会使用
- 为引入的变量使用别名：`from 模块名 import 变量 as 别名`

### 包（Package）

- 包也是一个模块，当我们模块中代码过多时，或者一个模块需要被分解为多个模块时，这时就需要使用到包
- 普通的模块就是一个 `.py` 文件，而包是一个文件夹
- 包中必须要一个一个`__init__.py`这个文件，这个文件中可以包含有包中的主要内容
- `__pycache__`是模块的缓存文件
- `.py` 代码在执行前，需要被解析器先转换为机器码，然后再执行,所以我们在使用模块（包）时，也需要将模块的代码先转换为机器码然后再交由计算机执行
- 为了提高程序运行的性能，python 会在编译过一次以后，将代码保存到一个缓存文件中,这样在下次加载这个模块（包）时，就可以不再重新编译而是直接加载缓存中编译好的代码即可

### Python 标准库

- 为了实现开箱即用的思想，Python 中为我们提供了一个模块的标准库
- 在这个标准库中，有很多很强大的模块我们可以直接使用，并且标准库会随 Python 的安装一同安装
- `sys` 模块，它里面提供了一些变量和函数，使我们可以获取到 Python 解析器的信息，或者通过函数来操作 Python 解析器
- `pprint` 模块它给我们提供了一个方法 `pprint()` 该方法可以用来对打印的数据做简单的格式化
- `sys.argv` 获取执行代码时，命令行中所包含的参数，该属性是一个列表，列表中保存了当前命令的所有参数
- `sys.modules` 获取当前程序中引入的所有模块
- modules 是一个字典，字典的 key 是模块的名字，字典的 value 是模块对象
- `sys.path` 是一个列表，列表中保存的是模块的搜索路径
- `sys.platform` 表示当前 Python 运行的平台
- `sys.exit()` 函数用来退出程序
- `os` 模块让我们可以对操作系统进行访问
- `os.environ`. 通过这个属性可以获取到系统的环境变量
- `os.system()` 可以用来执行操作系统的名字` os.system('dir') os.system('notepad')`

### 异常

- 程序在运行过程当中，不可避免的会出现一些错误，比如：使用了没有赋值过的变量，使用了不存在的索引，除 0 等
- 这些错误在程序中，我们称其为异常
- 程序运行过程中，一旦出现异常将会导致程序立即终止，异常以后的代码全部都不会执行

### 处理异常

- 程序运行时出现异常，目的并不是让我们的程序直接终止

- Python 是希望在出现异常时，我们可以编写代码来对异常进行处理

- try 语句
  
  ```python
  try:
  代码块（可能出现错误的语句）
  except 异常类型 as 异常名:
  代码块（出现错误以后的处理方式）
  else：
  代码块（没出错时要执行的语句）  
  finally:
  代码块（该代码块总会执行）
  ```
  
- try 是必须的；else 语句有没有都行；except 和 finally 至少有一个

- 可以将可能出错的代码放入到 try 语句，这样如果代码没有错误，则会正常执行

- 如果出现错误，则会执行 expect 子句中的代码，这样我们就可以通过代码来处理异常，避免因为一个异常导致整个程序的终止

### 异常的传播（抛出异常）

- 当在函数中出现异常时，如果在函数中对异常进行了处理，则异常不会再继续传播
  - 如果函数中没有对异常进行处理，则异常会继续向函数调用处传播,
  - 如果函数调用处处理了异常，则不再传播，如果没有处理则继续向调用处传播
  - 直到传递到全局作用域（主模块）如果依然没有处理，则程序终止，并且显示异常信息
- 当程序运行过程中出现异常以后，所有的异常信息会被保存一个专门的异常对象中，而异常传播时，实际上就是异常对象抛给了调用处
- `ZeroDivisionError` 类的对象专门用来表示除 0 的异常，`NameError` 类的对象专门用来处理变量错误的异常
- 在 Python 为我们提供了多个异常对象
- 如果 except 后不跟任何的内容，则此时它会捕获到所有的异常
- 如果在 except 后跟着一个异常的类型，那么此时它只会捕获该类型的异常
- `Exception` 是所有异常类的父类，所以如果 except 后跟的是 Exception，他也会捕获到所有的异常
- 可以在异常类后边跟着一个 `as xx` 此时 xx 就是异常对象
- 也可以自定义异常类，只需要创建一个类继承 Exception 即可
- 可以使用 raise 语句来抛出异常，raise 语句后需要跟一个异常类 或 异常的实例
- `raise Exception` 抛出异常的目的，告诉调用者这里调用时出现问题，希望你自己处理一下

### 文件（File）

- 通过 Python 程序来对计算机中的各种文件进行增删改查的操作
- `I/O(Input / Output)`
- 操作文件的步骤：
  1. 打开文件
  2. 对文件进行各种操作（读、写），然后保存
  3. 关闭文件

### 打开关闭文件

- 使用 `open 函数` 来打开一个文件
- 参数：
  - file 要打开的文件的名字（路径）
  - 返回值：返回一个对象，这个对象就代表了当前打开的文件
- 创建一个变量，来保存文件的名字， 如果目标文件和当前文件在同一级目录下，则直接使用文件名即可
- 在 windows 系统使用路径时，可以使用/来代替 \ ；或者可以使用 \\ 来代替 \ ；或者也可以使用原始字符串
- 表示路径，可以使用..来返回一级目录
- 如果目标文件距离当前文件比较远，此时可以使用绝对路径
  - 绝对路径应该从磁盘的根目录开始书写
- `file_obj = open(file_name) `打开 `file_name` 对应的文件
- 调用 `close()` 方法来关闭文件
- `open()` 打开文件时，默认是以文本文件的形式打开的，但是 `open()` 默认的编码为 None
- 所以处理文本文件时，必须要指定文件的编码

### 文件的读取

- 当我们获取了文件对象以后，所有的对文件的操作都应该通过对象来进行
- `read()` 方法，用来读取文件中的内容，它会将内容全部保存为一个字符串返回
- `with open() as file_obj`:在 with 语句中可以直接使用 `file_obj` 来做文件操作
  - 此时这个文件只能在 with 中使用，一旦 with 结束则文件会自动`close()`
- 如果要读取的文件较大的话，会一次性将文件的内容加载到内存中，容易导致内存泄漏，所以对于较大的文件，不要直接调用 `read()`
- `help(file_obj.read)`
- `read()` 可以接收一个 size 作为参数，该参数用来指定要读取的字符的数量，默认值为-1，它会读取文件中的所有字符
- 可以为 size 指定一个值，这样`read()`会读取指定数量的字符，
- 每一次读取都是从上次读取到位置开始读取的，如果字符的数量小于 size，则会读取剩余所有的，如果已经读取到了文件的最后了，则会返回' '空串
- `readline()`方法可以用来读取一行内容
- `readlines()` 方法用于一行一行的读取内容，它会一次性将读取到的内容封装到一个列表中返回

### 文件的写入

- 使用 `open()` 打开文件时必须要指定打开文件所要做的操作（读、写、追加）
- 如果不指定操作类型，则默认是 读取文件 ， 而读取文件时是不能向文件中写入的
- `r` 表示只读的
- `w` 表示是可写的，使用 `w` 来写入文件时，如果文件不存在会创建文件，如果文件存在则会截断文件，截断文件指删除原来文件中的所有内容
- `a` 表示追加内容，如果文件不存在会创建文件，如果文件存在则会向文件中追加内容
- `x` 用来新建文件，如果文件不存在则创建，存在则报错
- `-` 为操作符增加功能
- `r+` 即可读又可写，文件不存在会报错
- `w+`
- `a+`
- 例如：`with open(file_name , 'w' , encoding='utf-8') as file_obj:`
- `write()`来向文件中写入内容，如果操作的是一个文本文件的话，则 `write()` 需要传递一个字符串作为参数
- `write()` 方法会可以分多次向文件中写入内容，写入完成以后，该方法会返回写入的字符的个数

### 文件的其他操作

- `t` 读取文本文件（默认值）
- `b` 读取二进制文件
- `with open(file_name , 'rb') as file_obj:`
- 读取文本文件时，`size` 是以字符为单位的
- 读取二进制文件时，`size` 是以字节为单位
- 将读取到的内容写出来 定义一个新的文件
- `seek()` 可以修改当前读取的位置
- `seek()` 需要两个参数，第一个 是要切换到的位置，第二个 计算位置方式
- `seek` 计算位置可选值：0 从头计算（默认值）；1 从当前位置计算；2 从最后位置开始计算
- `tell()` 方法用来查看当前读取的位置
- `os.listdir()` 获取指定目录的目录结构，需要一个路径作为参数，会获取到该路径下的目录结构，默认路径为 . 当前目录
  - 该方法会返回一个列表，目录中的每一个文件（夹）的名字都是列表中的一个元素 `r = os.listdir()`
- `os.getcwd()` 获取当前所在的目录 `r = os.getcwd()`
- `os.chdir()` 切换当前所在的目录 作用相当于 `cd os.chdir('c:/')`
- `r = os.getcwd()`
- 创建目录，`os.mkdir("aaa")` 在当前目录下创建一个名字为 aaa 的目录
- 删除目录， `os.rmdir('abc') open('aa.txt','w')`
- 删除文件， `os.remove('aa.txt')`
- `os.rename('旧名字','新名字')` 可以对一个文件进行重命名，也可以用来移动一个文件， `os.rename('aa.txt','bb.txt')`
