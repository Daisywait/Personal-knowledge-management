#python
1.在命令行运行python文件
?
python hello_world.py
<!--SR:!2025-03-19,4,270-->

2.变量名只能包含？且什么可以打头？
?
字母、下划线、数字；字母、下划线，数字不可以
<!--SR:!2025-03-18,3,250-->

3.字符串用什么包裹？
?
单引号和双引号都行，而且可以互相嵌套，比如：“  ‘ ’  ”；‘  “ ”  ’
<!--SR:!2025-03-19,4,270-->

4.name="anne waitwhat"对名字字符串进行首字母大写打印；还有全部大写或全部小写
?
print(name.title())；print(name.upper())、print(name.lower())
<!--SR:!2025-03-19,4,270-->

5.用什么来拼接字符串？
?
加号+
<!--SR:!2025-03-19,4,270-->

6.在字符串中添加制表符（tab）和换行符
?
\t \n
<!--SR:!2025-03-19,4,270-->

7.删除字符串末尾多余的后面？开头？同时？
?
favorite_language = ' python '
favorite_language.rstrip()
' python'
favorite_language.lstrip()
'python '
favorite_language.strip()
'python'
<!--SR:!2025-03-18,3,250-->

8.使用什么表示乘方运算
?
两个乘号，比如3**2 -表示3的二次方得9-
<!--SR:!2025-03-19,4,270-->

9.使用什么将非字符串转换成字符串？
?
str
<!--SR:!2025-03-19,4,270-->

10.用一个列表包含几种自行车
?
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
<!--SR:!2025-03-20,3,250-->

11.返回列表中的最后一个元素、倒数第二个：
?
索引为-1、-2
<!--SR:!2025-03-19,4,270-->

12.将ducati元素附加到motorcycles列表末尾
?
append;
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)
motorcycles.append('ducati')
<!--SR:!2025-03-18,3,250-->

13.使用方法__可在motorcycles列表的任何位置添加新元素。为此，你需要指定__和__。motorcycles = ['honda', 'yamaha', 'suzuki']
?
motorcycles.insert(0, 'ducati')
print(motorcycles)
['ducati', 'honda', 'yamaha', 'suzuki']
<!--SR:!2025-03-18,3,250-->

14.如果知道要删除的元素在motorcycles列表中的位置，并且这个元素之后不再使用，可使用__语句来删除列表中的元素
?
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)
del motorcycles[0]
print(motorcycles)
['honda', 'yamaha', 'suzuki']
['yamaha', 'suzuki']
<!--SR:!2025-03-19,4,270-->

15.删除列表末尾的值，但是后期还需要使用它:motorcycles = ['honda', 'yamaha', 'suzuki']
?
popped_motorcycle = motorcycles.pop()
print(motorcycles)
print(popped_motorcycle)
<!--SR:!2025-03-18,3,250-->

16.想使用pop()删除列表中任何位置的元素：
?
first_owned = motorcycles.pop(0)
print('The first motorcycle I owned was a ' + first_owned.title() + '.')
<!--SR:!2025-03-18,3,250-->

17.如果知道要删除的值是什么，那么可以用
?
remove
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)
motorcycles.remove('ducati')
print(motorcycles)
['honda', 'yamaha', 'suzuki', 'ducati']
['honda', 'yamaha', 'suzuki']
<!--SR:!2025-03-20,3,250-->

18.remove根据值删除了之后还可以后续使用这个值是因为：
?
可以把删除的原因存储到一个变量里，例如：
too_expensive = 'ducati'
motorcycles.remove(too_expensive)
print(motorcycles)
print("\nA " + too_expensive.title() + " is too expensive for me.")
<!--SR:!2025-03-18,3,250-->

19.SyntaxError: Non-UTF-8 code starting with '\xb4' in file D:\wait_what\Documents\python_work\python\Chapter03\list_2.py on line 2, but no encoding declared; see https://peps.python.org/pep-0263/ for details
?
要在第一行添加：# coding=utf-8
<!--SR:!2025-03-18,1,210-->

20.对列表内的元素进行字母顺序排列，这种排序方式有什么特点？
?
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.sort()
永久改变列表顺序
<!--SR:!2025-03-18,3,250-->

21.对列表内的元素进行字母逆序排列
?
cars.sort(reverse=True)
<!--SR:!2025-03-18,3,250-->

22.字母顺序临时排序
?
cars = ['bmw', 'audi', 'toyota', 'subaru']
sorted(cars)
<!--SR:!2025-03-18,3,250-->

23.字母逆序临时排序
?
cars = ['bmw', 'audi', 'toyota', 'subaru']
print(sorted(cars,reverse=True))
<!--SR:!2025-03-19,2,230-->

24.列表逆序排列，有何特点？
?
cars.reverse(),永久性，但是再调用一次即可恢复
<!--SR:!2025-03-18,1,210-->

25.确定列表长度？
?
len(cars)
<!--SR:!2025-03-18,3,250-->

26.使用for循环来打印魔术师名单中的所有名字：magicians = ['alice', 'david', 'carolina']
?
for magician in magicians:
print(magician)
<!--SR:!2025-03-18,1,233-->

27.写for循环时容易出错的两个点：
?
①循环内的语句没有缩进②忘记在for语句后面加冒号

28.用什么可以打印1~5（不包含5）?
?
for value in range(1,5):
	print(value)

29.将range打印出来的数字形成一个列表：
?
numbers=list(range(1,6))
print(numbers)

30.用函数range打印10以内的偶数：
?
even_numbers = list(range(2,11,2))
print(even_numbers)

31.将前10个整数的平方一个一个加入到一个列表中：
?
squares = []
for value in range(1,11):
square = value ** 2
squares.append(square)
print(squares)
或者：squares.append(value ** 2)

32.找出digits列表中的最大值、最小值、总和：
?
max(digits)
min(digits)
sum(digits)

33.用列表解析将前10个整数的平方一个一个加入到一个列表中：
?
squares = [value**2 for value in range(1,11)]
print(squares)

34.players = ['charles', 'martina', 'michael', 'florence', 'eli']只打印列表前三个元素、2~4个元素：
?
print(players[0:3])、print(players[1:4])

35.print(players[:4])表示？print(players[2:])呢
?
从列表开头开始，打印至第四个元素(即索引3）；从索引2开始打印至列表的最后一个元素

36.输出名单上的最后三名队员？
?
可使用切片players[-3:]

37.![[Pasted image 20250318162218.png]]和![[Pasted image 20250318162248.png]]
的区别
?
第二个的语法实际上是让Python将新变量friend_foods关联到包含在my_foods中的列表，因此这两个变量都指向同一个列表，输出是第一个符合要求，而第二个不符合

38.如果需要存储的一组值在程序的整个生命周期内都不变，可使用？怎么使用
?
可以使用元组；比如一个矩形的长和宽固定不变：dimensions=(40,200)；注意要使用圆括号

39.元组可以进行重新赋值吗？对单个元素进行索引修改呢？
?
可以；不可以

40.


