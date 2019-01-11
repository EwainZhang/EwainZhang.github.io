---
layout: post
title: Python 
category: Python
tags: [Python ]
---

# chapter 2. Variables and data types
+ variable
+ the type of variable: string, number, list, tuple, dictionary

string: 由任意字节的字符组成，用单引号，双引号，三对双引号表示
number: Integer, float, complex, boolean

算数运算符
| operation | name |
| ------    |------|
| +         | plus | 
| -         | minus|
| *         | multiply|
| /         | divide|
| %         | module |
| **        | power |
| //        | exact division |

Boolean: True 可以用1替换， False可以用0替换
逻辑运算符
| operation | property|
|------     | ------- |
| and       | 1 and 1 = 1, other 0|
| or        | 0 or 0 = 0 , other 1|
| not       | not 0 = 1, not 1 = 0|

Binary
In the latest Python version , use 0b... denote binary number
```
>>>0b1110
14
```
二进制位运算符
| operation | rules |
|------     | ------ |
| x & y     | Does a "bitwise and". Each bit of the output is 1 if the corresponding bit of x AND of y is 1, otherwise it's 0.|
|  x \| y    | Does a "bitwise or". Each bit of the output is 0 if the corresponding bit of x AND of y is 0, otherwise it's 1|
|  x^y      | Does a "bitwise exclusive or". Each bit of the output is the same as the corresponding bit in x if that bit in y is 0, and it's the complement of the bit in x if that bit in y is 1.|
|  ~x       | Returns the complement of x - the number you get by switching each 1 for a 0 and each 0 for a 1. This is the same as -x - 1.|
| x << y        | Returns x with the bits shifted to the left by y places (and new bits on the right-hand-side are zeros). This is the same as multiplying x by 2**y.|
| x >> y        | Returns x with the bits shifted to the right by y places. This is the same as //'ing x by 2**y. |

chr(x)可以把x转为对应的ASCII码字符，x为十进制数。
Python: 
+ 八进制： 0o开头表示
+ 十六进制：0x开头表示


 Comparison Operators
 | Operator | Description |
 | ------   | ------      |
 | ==       | If the values of two operands are equal, then the condition becomes true.|
 | !=       | If values of two operands are not equal, then condition becomes true. |
 |  >       | If the value of left operand is greater than the value of right operand, then condition becomes true.|
 | <        | If the value of left operand is less than the value of right operand, then condition becomes true.|
 | >=       | If the value of left operand is greater than or equal to the value of right operand, then condition becomes true.|
 | <=       | If the value of left operand is less than or equal to the value of right operand, then condition becomes true. |
 
 Assignment operators
 | Operator | Description |
 |------    | ------      |
 | =        | c = a + b   |
 | +=       | x += y is x = x + y |
 | -=       | x -= y is x = x - y |
 | *=       | x *= y is x = x * y|
 | /=       | x /= y is x = x/y  |
 | %=       | x %= y is x = x% y |
 | **=      |   |
 | //=      |   |
 | <<=      | b1<<= m is b1 = b1 << m |
 | >>=      |    |
 | &=       |     |
 | \|=       |    |
 | ^=       |    |


数据类型转化


编码：
+ 单字节编码：ASCII：a,b,c... 对应于一个字节
+ 多字节编码：UTF-8: 中文每个汉字对应双字节

```python
# 多个变量赋值
one = two = three = 10
print(one, two, three)

one, two, three = 10,10,10
print(one, two, three) # print输出值为3个10

# string
name = 'Tom'
name1 = "Jerry"
name2 = ''' Sreck '''
print(name,name1, name2)

# basic operations of string 读取，合并，修改，删除
# 读取 [index] read
name = "Tom is a cat!"
name[1]  # 0
name[4:6] #读取下标为4-6的字符
name[:3]  #读取下标为0-3的字符
name[:]   #读取all string
name[::2] #从头到位，step 2
name[-1]  # from right to left, read the first character
name[-4:-1] #from right to left, read 倒数第四，第三，第二个字符

#binding using "+"
name = 'Tom'
job = "teacher"
record = name+ ',' + job
print(record)

#修改（读取子字符串并合并）
name = "Three cool cat"
new_name = name[:11] + 'dogs'
print(new_name)

#删除
del(name) #清除内存中的name

# other operations
# 获取字符串长度
hello = "Hello! Three cool cats"
len(hello)     #len function to derive length

#r/R 原始字符串控制符号
print("C:\back\name")
print(r"C:\back\name")

#重复输出字符串
print('Cat'*2)  #CatCat

#格式字符串
age = 10
print("Tom's name is %d"%(age))   # %d 为格式化整数

# NUmber
x = 5
y = 3
x% y # 2
x//y  # 1
5 /2 = 2

# complex
(1-2j) # 复数表示
(1-2j).real # real part
(1-2j).imag # imaginary part

# Boolean (True , False)

#binary
bin(14) #bin function 把十进制转化为二进制

# 数据类型转化
bin(x), oct(x), hex(x) #非负整数转化为二，八，十六进制数
chr(98), ord('a') # 十进制数转为ASCII字符， ASCII字符转为十进制
int(), float(), complex() #转化为整数，浮点数，复数的函数
str() #转化为字符串的函数
```

#Chapter 3. 条件分支与循环
+ if条件分支
+ while 循环
+ for 循环
+ break 语句
+ continue 语句

if 条件分支(If boolean_value1 is True, then perform module1)
单分支判断
```
if boolean_value1:
   module1
```
双分支判断
```
if boolean_value1:
   module1
else:
   module2
```
多条件分支判断
```
if boolean_value1:
   module1
elif boolean_value2:
   module2
else:
   module3
```
**We can use many elif in if staement, but else only appears once**

while循环(boolean_value1 is True, then perform, or, stop)
```
while boolean_value1:
      module1
```

for statement
```
for <variable> in <sequence>:
    module1
else:
    module2
```
variable接收sequence集合中获取的成员元素，循环一次接收一次。

循环控制语句
+ break statement: It terminates the current loop and resumes execution at the next statement, just like the traditional break statement in C.
+ continue statement: It returns the control to the beginning of the while loop.. The continue statement rejects all the remaining statements in the current iteration of the loop and moves the control back to the top of the loop.

循环和条件分支的逻辑判断
1. 变量、算术运算符、比较运算符、赋值运算符、位运算符
2. 成员运算符、身份运算符

membership operators
| operator | Description |
|------    | ------      |
| in       |The ‘in’ operator is used to check if a value exists in a sequence or not. Evaluates to true if it finds a variable in the specified sequence and false otherwise.|
| not in   | Evaluates to true if it does not finds a variable in the specified sequence and false otherwise.|

identity operators
|Operators | Descriptions|
|------    |------       |
| is       | Evaluates to true if the variables on either side of the operator point to the same object and false otherwise.|
| is not   | Evaluates to false if the variables on either side of the operator point to the same object and true otherwise.|


Operators Precedence in Python
| Operator | Description |
|------    | ------      |
| **       | Exponentiation |
| ~ + -    | Complement, unary plus and minus |
| * / % // | Multiply, divide, modulo and floor division |
| + -      | Addition and subtraction |
| >> <<    | Right and left bitwise shift |
| &        | Bitwise 'AND'         |
| ^  \|    | Bitwise exclusive \'OR\' and regular \'OR\' |
| < <= > >= | Comparison operators |
| ==   !=   | Equality operators |
| = %= /= //= += -= \*=  \**= | Assignment operators |
|is, is not | Identity operators |
| in, not in | Membership operators |
| not, and, or | Logical operators |

id(x): 用于查看变量x的内存地址
对于数字序列、字符串、列表、元组、字典等具有集合概念的对象，可以通过member operator 进行快速判断。for in

常见字符ASCII码的十进制数
0-9: 48-57
a-z: 97-122
A-Z: 65-90
Chinese character: >127

```python
if 2 is not in range(10)
print("2 is  not in this set!")

i =t = 1
i is t # True

```

# Chapter3 list and tuple
list: 是可变序列,是可以存储各种数据类型的集合，可以通过index获取列表元素
```
list1 = []
list2 =[a,b, c, d]
```
Basic operations
对集合元素进行增加、查找、修改、删除、合并操作等

add:
```
list1=[1,2,3]
list1.append(a)
list1.insert(m,a) #在索引为m的地方插入a
```
列表元素查找：
index(), in membership operator, index, slice

```
L.index(value,[start,[stop]])
```
L -- list
value -- the value we need to search
start -- the start of search
stop -- the final of search
[]   -- optionl, can be skipped

若查到元素，返回第一个查到的值；
若没找到，返回ValueError...


列表元素修改

列表元素删除
clear(), pop(), remove() methods and del function

```
L.clear()
L.pop([index])
L.remove(value)
del(L[index])
del(L)
```
pop()不跟index,默认从列表尾部弹出并删除一个元素
remove 要删除的值在列表中出现多次，一次只删除最左边的一个。


列表元素合并
extend() method, '+',
extend() 不会导致合并后的对象内存地址改变
+ 会导致合并后的对象内存地址改变


列表元素排序
sort(): 改变原有列表，L.sort(key=None, reverse=False)
reverse=False -- 升序排序
reverse=True -- 减序排序
key 参数影响排序规则, key = str.lower

sorted(): 不改变原有列表


列表其他操作方法
copy(), count(), reverse(), 列表解析
```
L.copy()
L.count(e) # e代表需要统计的元素
L.reverse() #对L的永久反向性记录
```

列表解析：
[expression for iter-val in iterable]
[expression for iter-val in iterable if cond_expr]

```
Nums = [i**2 for i in range(11) if i > 0]
print(Nums)
```
缺点：调试不方便


tuple
与列表的区别：
1.元组不能对其元素进行变动，而列表允许
2.元组用小括号表示，列表用中括号表示。

元组的基本格式及用法
```
test= (1,2,3)
test1 = (x,) #给一个元组变量赋值一个元素
```
省略小括号的元组定义及使用
```
name, age = 'Tom', 19
(name, age)    # result is ('Tom', 19)
name, age   # result is ('Tom', 19)
```

元组的基本操作
1. “+”，“=” 实现基本的定义、合并等操作
2. 借助元组自带的方法实现相关的操作
3. 借助Python内置函数实现相关操作

| Method | Descriptions |
| ------ | ------       |
| count  | 统计制定元素个数|
| index  | 返回指定元素的下标|

| function | Descriptions |
| ------   | ------       |
| len      |统计元组元素个数|
| max      |             |
| min      |             |
| tuple    | 将列表转化为元组|
| type     | 返回对象类型|
| del      | 删除整个元组对象|
| sum      | 对元组对象的所有元素求和|

```python
#add elements

# add in the final
list1 = [1,2,3]
list1.append(3.2)
print(list1)  # [1,2,3,3,2]

# insert method
list1 = [1,2,3]
list1.insert(0,2.3) #insert new element in the first place

#search
list1 = [1,2,3]
list1.index(1)

# in operator
list1 = [1,2,3]
1 in list1

# read value by index
list1=[1,2,3]
list1[2]

#read by slice
list1=[1,2,3]
list1[0:2]


# revise list
#指定下表，对对应元素进行赋值修改
list1 = [1,2,3]
list1[0] = 'a'
print(list1)


# 列表怒元素删除
#1 clear() method
list1  = [1,2,3]
list1.clear()
print(list1)

#2 pop() method
list1 = [1,2,2,3]
get_one = list1.pop()
print(get_one, list1)

# 3 remove()method
list1 = [1,2,2,3]
list1.remove(2)
print(list1)

# 4 del function
list1 = [1,2,2,3,3]
del(list1[1])
del(list1)


#列表元素合并
list1 =  [1,2,3]
list2 = [4,5,6]
list1.extend(list2)
print(list1)
id(list1)
list1 += list2
print(list1)
id(list1)
```

# Chapter 5. dictionary
Dict 是可变的无序集合，以key-value为基本元素的集合
字典的表示
```
{}
d1 = {'Tom':29}
len(d1)     # 1
```
Dictionary's key and value
1. the setting of the key: 唯一、不可变性
2. the setting of the value: Python支持的任何对象

```
d3 = {1:'car', 2:'bus', 2:'bus'}
lend(d3)       # 2
```

字典的基本操作方法
1. 字典元素增加: 赋值, setdefault()
2. 字典值查找
3. 字典值修改
4. 字典元素删除
5. 字典遍历操作
6. 其他操作

```
# 元素增加  D[k] = value, k为指定的键
d1 = {'Tom':2, 'Jim':5}
d1['Mike'] = 8
d1

# setdefalut() method
d1 = {'Tom':2, 'Jim':5}
d1.setdefault('Alice',10)
d1
```
用setdefault method新增key-value时，若key存在，显示已存在的键的值。

字典值查找
1. D[k] 查找,指定键不存在时报错
2. D.get(key,[value]) 查找,指定键不存在时返回空值

字典值的修改
1. 赋值修改: D[key] = value
2. update(): D.update(d1), d1为提供新内容的字典，若d1里提供的键在D里存在，则更新值，否则，新增key-value

字典元素删除
1. del(D[key])
2. pop(): D.pop(key,[value])
3. popitem(): D.popitem(), 随即返回一个key-value tuple,并在字典里删除对应元素

字典遍历操作
1. items() method遍历所有键值对: D.items(),以tuple形式返回字典的所有元素。
```
d1 = {1:'a', 2:'b', 3:'c', 4:'d'}
for get_one in d1.items():
    print(get_one)
```
2. 遍历所有键
```
# 1. 利用字典变量循环遍历
d1 = {1:'a', 2:'b', 3:'c', 4:'d'}
for gets in d1:
    print(gets)
    
# 2. key() method获得字典键
d1 = {1:'a', 2:'b', 3:'c', 4:'d'}
for gets1 in d1.keys():
    print(gets1)
    
```
3. 遍历所有的值
```
#1 通过键遍历值
d1 = {1:'a', 2:'b', 3:'c', 4:'d'}
for get_key in d1:
    print(d1[get_key])
    
# 2 values() method
d1 = {1:'a', 2:'b', 3:'c', 4:'d'}
for get_v in d1.values():
    print(get_v)
    
```

4. 其他操作: D.clear(), D.copy(), in membership operator

copy()赋值时，可以避免字典变量之间直接赋值指向同一个地址的问题

fromkeys(): D.fromkeys(iterable), iterable代表列表对象，用于指定字典键,生成D的键默认Null


字典嵌套
1.字典嵌入字典:多重关系，多行记录
2.列表嵌入字典
3. 字典嵌入列表

# Chapter 6. function
The definition of function
```
def function_name([parameter]):
    function_body
[return value]   
```
1. function without parameter
2. function with parameters
3. function with parameters and return values

不带return语句的函数，默认返回noun值

把函数放到模块中:
1. module以.py结尾
2. 调用函数模块: 
导入整个模块:import <module_name> , 必须保证调用文件和模块文件在同一个文件夹下，否则会出现ModuleNotFoundError
导入指定函数: from <module_name> import functionname1,[functionname2, ...]
导入所有函数: from <module> import*

module and functions' alias (as statement)
模块名(函数名) as alias

as语句除了解决名称过长问题，还可用于解决函数命名冲突问题。
```
import test_functions as t1
t1.find_factor(8)
```

模块搜索路径
当module和调用文件不再同一个文件夹下，需要临时指定模块路径
```
import sys
sys.path[0] = 'full pathname'
from <module> import *
.......
```
原理:代码解释器会先搜索调用文件所在目录下是否存在module, 其次搜索指定的模块路径。

## 参数的变化
1. 位置参数
2. 关键字参数
3. 不定长参数

位置参数:传递参数值时，必须和函数定义的参数一一对应,位置不能打乱
```
def test1(name, age):
    print("name%S, age%s" % (name, str(age)))
test1('Tom', 11)
```

关键字参数:
为了避免传递值出错, 采用“参数名 = 值”的方式调用函数
```
def test1(name, age):
     print("name%S, age%s" % (name, str(age)))
test1(name = 'Tom', age = 20)
test1(age = 20, name = 'Tom')
test1('Tom', age = 20) # 部分指定时，左边的可以不指定,从右边指定。
test1(name ='Tom', 20) # incorrect
```

默认值
为参数预先指定默认值，当没有给参数传值时，该参数自动选择默认值，赋值情况需要避免

不定长参数* **
1. 传递任意数量的参数值
functionname([param1, param2, ...,] *paramX)
带*的paramX可以接受任意数量的值, 但是一个自定义函数只能有一个带 star 的参数值，而且只能放置在最右边的参数中。
2. 传递任意数量的键值对
functionname([param1, param2, ...,] **paramX)


自定义函数可以传递list, tuple and dictionary
函数传递对象:
1.可变对象：在函数里进行值修改, 函数内外还是同一个对象,但是值同步发生变化，例如, list and dictionary
2.不可变对象: 在函数里进行值修改, 会变成新的对象(在内存产生新的地址)。e.g. number, string, tuple


函数变量作用域:
1.全局变量和局部变量
2. global 关键字
3. 闭包closure
4. nonlocal 关键字

根据变量可供访问的范围分为Global varibale and local variable
Global variable: 从赋值定义开始,后续代码都可以访问该变量
local variable: 只能在被定义的函数或类内部才能被访问。

匿名函数:
lambda[para1, para2, ...]:expression
1. lambda后面没有跟函数名
2. 参数可选，任何类型的
3. expression实现匿名函数功能的过程, 并返回操作结果
4. 整个匿名函数在一行内实现所有定义

```
lambda x, y: x*y
<function<lambda> at ....>   #按 enter 键执行的结果
a = lambda x, y: x*y
a(2,3)
```

递归函数:

```python
# function without parameters
def function_name():
  function_body
  
# example find 10's factors
def func_no_para():
  i = 1
  num = 10
  print("%d's factors are: " % num)
  while i <= num:
    if num % i == 0:
      print("%d" % i)
    i += 1
#==================================== 自定义函数结束，下面调用自定义函数
func_no_para()                        # 调用自定义函数
tt = type(func_no_para)               # 检查是否是函数类型
print(tt)                          


# 2. function with parameters
def function_name(parameter):
  function_body
  
def find_factor(nums):
  i = 1
  str1 = ' '
  print("%d's factors are: " % nums)
  while i <= num:
    if num % i == 0:
      str1 = str1 + ' ' + str(i)
      i += 1
  print("%d" % i)
# ==================================== 
num2_L = [10, 15, 18, 25]           #定义四个整数的列表
i = 0
num_len = len(num2_L)
while i < num_len:
  find_factor(num2_L[i])
  i += 1


# 3. function with return value
def find_factor(nums):
  i = 1
  str1 = ' '
  print("%d的因数是: " % nums)
  while i < nums:
    if nums % i == 0:
      str1 = str1 + '' + str(i)
      i += 1
      return str1              #返回因数字符串
      
# ================================== 调用自定义函数
num2_L = [10, 15, 18, 25]
i = 0
num_len = len(num2_L)
return_str = ''
while i < num_len:
  return_str = find_factor(num2_L[i])
  print("%d的因数是: %s" % (num2_L[i], return_str))
  i += 1
  
  
# 自定义函数的完善: 1.建立相应的函数文档，2.程序的健壮性

#建立函数文档
def find_factor(nums):
  '''
  find_functor是自定义函数
  nums是一个传递正整数的参数
  以字符串的形式返回一个正整数的所有因数
  '''     #用一对三个单引号来包括描述文档
   i = 1
  str1 = ' '
  print("%d的因数是: " % nums)
  while i < nums:
    if nums % i == 0:
      str1 = str1 + '' + str(i)
      i += 1
      return str1        
# =============================
help(find_factor)             #获取find_factor函数的帮助信息


# 2 健壮性 若向find_factor(nums) 传递一个字符、符号会怎样， 报错， 为了避免报英文错误，我们需要加入如下代码
def find_factor(nums):
    """
      find_functor是自定义函数
      nums是一个传递正整数的参数
      以字符串的形式返回一个正整数的所有因数
      """  # 用一对三个单引号来包括描述文档
    if type(nums) != int:
        print("输入值类型错误，必须是整数!")
        return # 终止函数执行
    if nums <= 0:
        print("输入值范围错误，必须是正整数!")
        return
    i = 1
    str1 = ''
    print("%d的因数是: " % nums)
    while i <= nums:
        if nums % i == 0:
            str1 = str1 + ' ' + str(i)
        i += 1
    return str1
    

# ===============================
#传递任意数量参数值
def watermelon(name, *attributes):
    print(name)
    print(type(attributes))
    description = ''
    for get_t in attributes:
        description += ' ' + get_t
    print(description)

# ================================= 调用函数
watermelon('西瓜', '甜', '圆形', '绿色')

# 传递任意数量键值对
def watermelon(name, **attributes):
    print(name)
    print(type(attributes))
    return attributes

# ==========================
print(watermelon('西瓜', taste = 'sweat', shape='sphere', color='green'))

#函数传递对象
def EditFruit(name, attributes):
    attributes[0] = attributes[0] * 0.9
    return attributes
# 调用 EditFruit function


attri_L = [21, 'sweat', 'sphere', 'green']
get_L = EditFruit('watermelon', attri_L.copy()) # copy() method 复制列表但是改变内存地址
print(get_L)
print(attri_L)


#全局、局部、闭包变量, 使用范围全局变量>闭包变量>局部变量
j = 5   # 全局变量j
def sum0():   # 外部函数sum
  k = 2       # 闭包变量k
  def sum1():
    i = k + j  #局部变量 i
    return i
  return sum1()

```

# class
类的相关注意点
1. class keyword
2. class name首字母要大些(约定)
3. class 第一行 
```
class name():
```
4. 类文档说明:三个双引号成对引用
5. class function: In class, are also called Method, including __init__ and volume function
6. 保留函数 __init__ 和self 关键字

**convention: 带小括号的叫方法, 不带小括号的叫函数, __init__() 叫构造方法**

__init__ 函数和self 关键字的作用：为类的实例化作准备
最简使用格式
```
def __init__(self):
```
如果实例要传递多个参数
```
def __init__(self length1, width1, height1)
my_box1 = Box1(10, 10, 10)       #参数传递
```
类里的函数要变成实例可以调用的方法也要用self
```
def volume(self)
```

实例相关：
1. 实例实现, 通过实例化过程实现，实质是在内存中建立一个独立的实例对象，例如 
```
my_box1 = Box1(10, 10, 10)
```
2. 多实例: 同一个类给多个实例对象赋值
```
my_box1 = Box1(10, 10, 10)  #第一个实例
print()
my_box2 = Box1(5, 15, 10)   # 第二个实例
print()
```
3. 实例的属性、方法
属性调用: 实例名.属性名
方法调用: 实例名.方法名
```
tt = my_box1.length
print(tt)

my_box1 = Box1(10, 10, 10)
my_box1.volume()
```

## 属性使用
属性值初始化:
1. 在__init__ 里直接初始化， 直接给self.length等赋值
2. 传递参数初始化(例子里做的)

属性值修改:
1.直接修改
2. 通过方法对属性值修改, 见代码

把类赋值给属性


## 类改造问题
1. 类的继承(Inheritance)
2. 方法的重写

类的继承:就是在继承原有类的基础上,增加新的功能(属性或方法), 形成新的子类,被继承的叫父类

**继承可以多层级继承，Box1为父类， Box2 is Box1's child class, Box3 is Box2's child class**

重写方法:当父类方法满足不了实际需要时,可以在子类中重写方法
e.g. After the area function, we need to revise the volume() method
```
def volume(self, num= 1):        #只要求函数名和父类的函数名一致
return self.length*self.width*self.height
```

## 私有
类里的变量或函数只能被这个类自身访问,需要引入private, 只要在名字前面加上双下划线

## 将类放到模块中
在主程序中调用类的方法和调用函数的方法一致

## 类总结
1.类分为动态类和静态类
2.实例由动态类生成, 核心是属性和方法

| 现实世界对象 | 动态类 | 实例 |
| ------       | ------ | ------|
| 特性         | 数据   | 属性  |
| 行为         | 函数   | 方法  |


静态类和动态类的关键区别
1. no self keywords
2. Do not pass parameters by class name
3. Do not support __init__ intiation function
4. 不能被实例化，但可以集成变量或函数, 是一个带结构的数据类型

静态类可以集成变量或函数，然后存放于类模块，供其他代码通过类名直接调用
对于需要实例化的动态类，提倡通过self关键字属性化后再调用，这样可以确保各个实例的属性值互不干扰。

面向对象编程的核心方法:封装、继承、多态

其他注意事项
1. 不要属性与方法重名：方法:驼峰式命名 CountBox(), 属性用一个小写字母加英文全拼 iAge
2. 不要直接使用动态类内部的数据变量
3. 当类变的庞大或会变得庞大时，应该把类合理拆分
4. 可以在类里引用外面已经定义的函数。

```python
class Box1():    # 类定义，类名为Box1
    """the class of computing volume of cubic"""
    def __init__(self, length1, width1, height1):  # 传递类参数的保留函数 __init__,注意每边是双下划线
        self.length = length1      # 长数据变量
        self.width = width1        # 宽数据变量
        self.height = height1      # 高数据变量

    def volume(self):              # 求立方体体积的函数，并供实例调用
        return self.length*self.width*self.height
# =============================================== 上面为类定义, 下面开始调用类, 并建立对应实例


my_box1 = Box1(10, 10, 10)       # 通过Box1类赋值建立对应的一个实例my_box1
print("The volume is %d"%(my_box1.volume()))   # 通过实例调用 volume方法求体积并打印

#修改类的属性

# 1 直接修改
class Box1():
    """求立方体的class"""
    def __init__(self):
        self.length = 0
        self.width = 0
        self.height = 0
# ============================== 主程序调用Box1类, 并创建B1, B2实例


B1 = Box1()
print(B1.length)
B1.length =10
print(B1.length)
B2 = Box1()
B2.length = 20
print(B2.length)




#通过方法修改类的属性
class Box1():
    """求立方体的类"""
    def __init__(self):
        self.length = 0
        self.width = 0
        self.height = 0
    def setNewLength(self,length1):      # 定义修改属性length 的函数
        self.length = length1
# =============================================


b1 = Box1()
b1.setNewLength(15)
print(b1.length)



# 把类赋值给属性
#当类的某一属性比较复杂时，可以考虑把与该属性相关的功能放到一个class中。
# 把颜色类赋值给颜色属性


# 类的继承
class Box1():    # 定义父类 Box1
    """the class of computing volume of cubic"""
    def __init__(self, length1, width1, height1):  # 传递类参数的保留函数 __init__,注意每边是双下划线
        self.length = length1      # 长数据变量
        self.width = width1        # 宽数据变量
        self.height = height1      # 高数据变量

    def volume(self):              # 求立方体体积的函数，并供实例调用
        return self.length*self.width*self.height
# ==================================================


class Box2(Box1):                   # 继承Box1定义子类Box2
    def __init__(self, length1, width1, height1):  #子类重新定义__init__
        super().__init__(length1, width1, height1) # super实现子类与父类的关联
        self.color = "white"           # 增加颜色属性
        self.material = "paper"        # 增加材料属性
        self.type = "fish"             # 增加种类属性

    def area(self):                    # 增加求表面积函数
        re = self.length * self.width + self.length * self.height + self.width * self.height
        return re*2
# ================================================= 主程序调用类及实例


my_box2 = Box2(10, 10, 10)              # 通过子类Box2创建my_box2实例
print("立方体体积是%d" % my_box2.volume())  # 通过子类调用父类 volume() 方法
print("立方体表面积是%d" % my_box2.area())
print("Box颜色 %s, 材料 %s, 类型 %s" % (my_box2.color, my_box2.material, my_box2.type))


# private
class TeatPrivate():
  def __init__(self):
    self.__say = 'ok'         #在实例处, __say属性实例讲无法看到
  def p(self):
    print(self.__say)         #在实例处, __p1() 方法实例将无法看到
  def __p1(self):
    print(self.__say)
#==========================  主程序调用类实例


show = TeatPrivate()
show.p()
```