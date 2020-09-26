1. ## **每个模块使用的函数意义**
### P10-11的模块查询及代码运行
* ## **sys模块**
### import sys 导入sys模块 sys.platform 访问你所运行的系统 
```
>>> import sys
>>> sys.platform
'win32'
```
* ## **os模块**
### import os 导入os模块 os.getcwd() 调用功能 
```
>>> import os
>>> os.getcwd()
'C:\\Users\\86137\\AppData\\Local\\Programs\\Python\\Python38-32'
```
* ## **datetime模块**
### import datetime 导入datetime模块 datetime.date,tody() 查看今天日期 
```
>>> import datetime
>>> datetime.date.today()
datetime.date(2020, 9, 20)
```
```
>>> datetime.date.today().day
>>> datetime.date.today().month
>>> datetime.date.today().year
```
### 此三行的代码分别为今天日期的组成成分（日，月，年）
```
>>> datetime.date.isoformat(datetime.date.today())
‘2020-9-20’
```
### 今天的日期转换为一个字符串
* ## **time模块**
### import time 导入time模块  time.strftime()以什么方式显示时间
```
>>> time.strftime("%H:%M")
'14:36'
```
* ## **HTML模块** 
###  import html 导入html模块 
```
>>> import html 
>>> html.escape("This HTML fragment contains a <script>script</script> tag.") 'This HTML fragment contains a &lt;script&gt;script&lt;/script&gt; tag.'
>>> html.unescape("I &hearts; Python's &lt;standard library&gt;.") "I  Python's <standard library>."
```
### 与HTML编码文本的来回转换。
2. ## **尝试理解if 、else、elif是什么？什么是代码块，并运行P16-18代码**
### if语句判断是对的，就把print语句执行，如果if判断是错的，不要执行if的内容，把else内容执行 elif是else if的缩写
### 一个函数（function）或一个类（class）定义、一个模块（module）都是代码块，一个代码块可以单独运行。
* ##p16-18的代码
```
>>> from datetime import datetime
>>> odds = [1,3,5,7,9,11,13,15,17,19,21,23,25,27,29,31,33,35,37,39,41,43,45,47,49,51,53,55,57,59]
right_this_minute = datetime.today().minute
if right_this_minute in odds:
    print("This munute seems a little odd.")
else:

        print("not an odd minute.")
```
### 运行结果 not an odd minute.
```
>>> import datetime
>>> today=datetime.date.today()
>>> 
>>> if today=="sunday":
    print("recover")
elif today=="saturday":
    print('party')
else :
    print('work,work,work')
```
### 运行结果 work,work,work
3. ## **尝试理解什么是迭代，并运行P24-25 for循环、range循环代码**
### Python中的迭代是指通过重复执行的代码处理相似的数据集的过程，并且本次迭代的处理数据要依赖上一次的结果继续往下做，上一次产生的结果为下一次产生结果的初始状态，如果中途有任何停顿，都不能算是迭代。
```
>>> for i in [1, 2, 3]:  print(i) 1 SyntaxError: invalid syntax 
>>> for i in [1, 2, 3]:  print(i) 

1 
2 
3
```
```
>>> for ch in "Hi!":  
          print(ch)  
H 
i 
!
```
### 循环5次
```
>>> for num in range(5):
	print('Head First Rocks!')

	
Head First Rocks!
Head First Rocks!
Head First Rocks!
Head First Rocks!
Head First Rocks!
```
### range实验
```
>>> range(5)
range(0, 5)
>>> list(range(5))
[0, 1, 2, 3, 4]
>>> list(range(5,10))
[5, 6, 7, 8, 9]
>>> list(range(0,10,2))
[0, 2, 4, 6, 8]
>>> list(range(10,0,-2))
[10, 8, 6, 4, 2]
>>> list(range(10,0,2))
[]
>>> list(range(99,0,-1))
[99, 98, 97, 96, 95, 94, 93, 92, 91, 90, 89, 88, 87, 86, 85, 84, 83, 82, 81, 80, 79, 78, 77, 76, 75, 74, 73, 72, 71, 70, 69, 68, 67, 66, 65, 64, 63, 62, 61, 60, 59, 58, 57, 56, 55, 54, 53, 52, 51, 50, 49, 48, 47, 46, 45, 44, 43, 42, 41, 40, 39, 38, 37, 36, 35, 34, 33, 32, 31, 30, 29, 28, 27, 26, 25, 24, 23, 22, 21, 20, 19, 18, 17, 16, 15, 14, 13, 12, 11, 10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
```
4. ## **学习掌握random、time模块，结合循环、迭代尝试完成P43 （尽量不要翻看P44答案）代码作业**
### random模块
```
>>> import random
>>> random.randint(1,60)
26
>>> random.randint(1,60)
21
>>> random.randint(1,60)
50
```
* 从99倒数到0
* 显示当前迭代的歌词
* 查看
* 结束歌词
* 如果不是否则
* 把下一个编号记到另一个变量中
* 如果喝最后一瓶
* 修改成单数
* 写完最后一句歌词
* 打印一个空行



