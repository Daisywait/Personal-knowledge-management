#python
1.在命令行运行python文件
?
python hello_world.py
<!--SR:!2025-04-04,15,290-->

2.变量名只能包含？且什么可以打头？
?
字母、下划线、数字；字母、下划线，数字不可以
<!--SR:!2025-03-31,11,270-->

3.字符串用什么包裹？
?
单引号和双引号都行，而且可以互相嵌套，比如：“  ‘ ’  ”；‘  “ ”  ’
<!--SR:!2025-04-04,15,290-->

4.name="anne waitwhat"对名字字符串进行首字母大写打印；还有全部大写或全部小写
?
print(name.title())；print(name.upper())、print(name.lower())
<!--SR:!2025-04-03,14,290-->

5.用什么来拼接字符串？
?
加号+
<!--SR:!2025-04-05,16,290-->

6.在字符串中添加制表符（tab）和换行符
?
\t \n
<!--SR:!2025-04-03,14,290-->

7.删除字符串末尾多余的后面？开头？同时？
?
favorite_language = ' python '
favorite_language.rstrip()
' python'
favorite_language.lstrip()
'python '
favorite_language.strip()
'python'
<!--SR:!2025-03-22,2,230-->

8.使用什么表示乘方运算
?
两个乘号，比如3**2 -表示3的二次方得9-
<!--SR:!2025-04-05,16,290-->

9.使用什么将非字符串转换成字符串？
?
str
<!--SR:!2025-04-03,14,290-->

10.用一个列表包含几种自行车
?
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
<!--SR:!2025-03-31,11,270-->

11.返回列表中的最后一个元素、倒数第二个：
?
索引为-1、-2
<!--SR:!2025-04-04,15,290-->

12.将ducati元素附加到motorcycles列表末尾
?
append;
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)
motorcycles.append('ducati')
<!--SR:!2025-03-30,10,270-->

13.使用方法__可在motorcycles列表的任何位置添加新元素。为此，你需要指定__和__。motorcycles = ['honda', 'yamaha', 'suzuki']
?
motorcycles.insert(0, 'ducati')
print(motorcycles)
['ducati', 'honda', 'yamaha', 'suzuki']
<!--SR:!2025-03-28,8,250-->

14.如果知道要删除的元素在motorcycles列表中的位置，并且这个元素之后不再使用，可使用__语句来删除列表中的元素
?
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)
del motorcycles[0]
print(motorcycles)
['honda', 'yamaha', 'suzuki']
['yamaha', 'suzuki']
<!--SR:!2025-03-22,2,250-->

15.删除列表末尾的值，但是后期还需要使用它:motorcycles = ['honda', 'yamaha', 'suzuki']
?
popped_motorcycle = motorcycles.pop()
print(motorcycles)
print(popped_motorcycle)
<!--SR:!2025-03-22,2,230-->

16.想使用pop()删除列表中任何位置的元素：
?
first_owned = motorcycles.pop(0)
print('The first motorcycle I owned was a ' + first_owned.title() + '.')
<!--SR:!2025-03-30,10,270-->

17.如果知道要删除的值是什么，那么可以用
?
remove
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)
motorcycles.remove('ducati')
print(motorcycles)
['honda', 'yamaha', 'suzuki', 'ducati']
['honda', 'yamaha', 'suzuki']
<!--SR:!2025-03-29,9,250-->

18.remove根据值删除了之后还可以后续使用这个值是因为：
?
可以把删除的原因存储到一个变量里，例如：
too_expensive = 'ducati'
motorcycles.remove(too_expensive)
print(motorcycles)
print("\nA " + too_expensive.title() + " is too expensive for me.")
<!--SR:!2025-03-22,2,230-->

19.SyntaxError: Non-UTF-8 code starting with '\xb4' in file D:\wait_what\Documents\python_work\python\Chapter03\list_2.py on line 2, but no encoding declared; see https://peps.python.org/pep-0263/ for details
?
要在第一行添加：# coding=utf-8
<!--SR:!2025-03-23,3,230-->

20.对列表内的元素进行字母顺序排列，这种排序方式有什么特点？
?
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.sort()
永久改变列表顺序
<!--SR:!2025-03-30,10,270-->

21.对列表内的元素进行字母逆序排列
?
cars.sort(reverse=True)
<!--SR:!2025-04-01,12,270-->

22.字母顺序临时排序
?
cars = ['bmw', 'audi', 'toyota', 'subaru']
sorted(cars)
<!--SR:!2025-03-31,11,270-->

23.字母逆序临时排序
?
cars = ['bmw', 'audi', 'toyota', 'subaru']
print(sorted(cars,reverse=True))
<!--SR:!2025-03-27,7,250-->

24.反转列表的排列顺序，有何特点？（不用sort)
?
cars.reverse(),永久性，但是再调用一次即可恢复
<!--SR:!2025-03-22,1,170-->

25.确定列表长度？
?
len(cars)
<!--SR:!2025-04-01,12,270-->

26.使用for循环来打印魔术师名单中的所有名字：magicians = ['alice', 'david', 'carolina']
?
for magician in magicians:
print(magician)
<!--SR:!2025-03-23,3,253-->

27.写for循环时容易出错的两个点：
?
①循环内的语句没有缩进②忘记在for语句后面加冒号
<!--SR:!2025-03-24,3,254-->

28.用什么可以打印1~5（不包含5）?
?
for value in range(1,5):
	print(value)
<!--SR:!2025-03-23,2,234-->

29.将range打印出来的数字形成一个列表：
?
numbers=list(range(1,6))
print(numbers)
<!--SR:!2025-03-23,3,254-->

30.用函数range打印10以内的偶数：
?
even_numbers = list(range(2,11,2))
print(even_numbers)
<!--SR:!2025-03-23,3,254-->

31.将前10个整数的平方一个一个加入到一个列表中：
?
squares = []
for value in range(1,11):
square = value **  2
squares.append(square)
print(squares)
或者：squares.append(value ** 2)
<!--SR:!2025-03-23,2,234-->

32.找出digits列表中的最大值、最小值、总和：
?
max(digits)
min(digits)
sum(digits)
<!--SR:!2025-03-24,3,254-->

33.用列表解析将前10个整数的平方一个一个加入到一个列表中：
?
squares = [value**2 for value in range(1,11)]
print(squares)
<!--SR:!2025-03-23,2,234-->

34.players = ['charles', 'martina', 'michael', 'florence', 'eli']只打印列表前三个元素、2~4个元素：
?
print(players[0:3])、print(players[1:4])
<!--SR:!2025-03-24,3,254-->

35.print(players[:4])表示？print(players[2:])呢
?
从列表开头开始，打印至第四个元素(即索引3）；从索引2开始打印至列表的最后一个元素
<!--SR:!2025-03-23,3,254-->

36.输出名单上的最后三名队员？
?
可使用切片players[-3:]
<!--SR:!2025-03-23,3,254-->

37.![[Pasted image 20250318162218.png]]和![[Pasted image 20250318162248.png]]
的区别
?
第二个的语法实际上是让Python将新变量friend_foods关联到包含在my_foods中的列表，因此这两个变量都指向同一个列表，输出是第一个符合要求，而第二个不符合
<!--SR:!2025-03-23,3,254-->

38.如果需要存储的一组值在程序的整个生命周期内都不变，可使用？怎么使用
?
可以使用元组；比如一个矩形的长和宽固定不变：dimensions=(40,200)；注意要使用圆括号
<!--SR:!2025-03-23,3,254-->

39.元组可以进行重新赋值吗？对单个元素进行索引修改呢？
?
可以；不可以
<!--SR:!2025-03-24,3,254-->

40.要判断特定的值是否已包含在列表中，可使用关键字
?
in
<!--SR:!2025-03-23,3,254-->

41.确定特定的值未包含在列表中很重要；在这种情况下，可使用关键字
?
not in。
<!--SR:!2025-03-23,3,254-->

42.将列表里的字符都进行lower处理：
?
curren_users=['Alice','wait','JOHN']
current.users=[u.lower() for u in current_users]
<!--SR:!2025-03-24,3,256-->

43.写一个包含外星人颜色和分数的字典，并且各自打印和打印整个字典出来：
?
alien_0 = {'color': 'green','points':5}
print(alien_0['color'])
print(alien_0['points'])
print(alien_0)
<!--SR:!2025-03-24,3,256-->

44.在字典alien_0中添加两项信息：外星人的x坐标和y坐标
?
alien_0['x_position'] = 0
alien_0['y_position'] = 25
<!--SR:!2025-03-24,3,256-->

45.创建一个空字典
?
alien_0 = {}
<!--SR:!2025-03-24,3,256-->

46.将字典中的一个外星人从绿色改为黄色：
?
alien['color']='yellow'
<!--SR:!2025-03-24,3,256-->

47.从字典alien_0中删除键'points'及其值：
?
del alien_0['points']
<!--SR:!2025-03-24,3,256-->

48.如何遍历字典中的所有键值对？有哪三个重要的构成？
?
for key, value in user_0.items():
<!--SR:!2025-03-24,3,256-->

49.如何遍历字典中所有的键？
?
for key in user_0.keys()
<!--SR:!2025-03-24,3,256-->

50.如何遍历字典中所有的值？
?
for value in user_0.values()
<!--SR:!2025-03-24,3,256-->

51.如何对字典中的键按字母顺序排列输出
?
for name in sorted(favorite_languages.keys()):
print(name.title() + ", thank you for taking the poll.")
<!--SR:!2025-03-22,1,236-->

52.如何对字典中的值精简输出，不重复：
?
for language in set(favorite_languages.values()):
print(language.title())
<!--SR:!2025-03-22,1,236-->

53.TypeError: 'int' object is not iterable什么意思？
?
指python
num = 5
for i in num:  # 错误！int 不可迭代
    print(i)

54.列表中存储字典,并且打印出来：
?
alien_0 = {'color': 'green', 'points': 5}
alien_1 = {'color': 'yellow', 'points': 10}
alien_2 = {'color': 'red', 'points': 15}
aliens = [alien_0, alien_1, alien_2]
for alien in aliens:
print(alien)

55.在字典pizza中存储toppings列表,并且打印出来：
?
pizza = { 
  'crust': 'thick', 
  'toppings': ['mushrooms', 'extra cheese'], 
  }
for topping in pizza[[['toppings' ]]]:
print("\t" + topping)

56.字典中的items()只是返回：
?
key和value两个类型值，是键值对的形式，不是有多少个键值对

57.字典中存字典,并且访问字典里面的字典中的值：
?
users = {
'aeinstein': {
'first': 'albert',
'last': 'einstein',
'location': 'princeton',
},
'mcurie': {
'first': 'marie',
'last': 'curie'
'location': 'paris',
},
}
for username, user_info in users.items():
print("\nUsername: " + username)
full_name = user_info['first'] + " " + user_info['last']
location = user_info['location']

58.

