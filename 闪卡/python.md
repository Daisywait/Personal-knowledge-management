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
<!--SR:!2025-03-29,7,250-->

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
<!--SR:!2025-03-27,5,250-->

15.删除列表末尾的值，但是后期还需要使用它:motorcycles = ['honda', 'yamaha', 'suzuki']
?
popped_motorcycle = motorcycles.pop()
print(motorcycles)
print(popped_motorcycle)
<!--SR:!2025-03-29,7,250-->

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
<!--SR:!2025-03-29,7,250-->

19.SyntaxError: Non-UTF-8 code starting with '\xb4' in file D:\wait_what\Documents\python_work\python\Chapter03\list_2.py on line 2, but no encoding declared; see https://peps.python.org/pep-0263/ for details
?
要在第一行添加：# coding=utf-8
<!--SR:!2025-04-02,10,250-->

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
<!--SR:!2025-03-29,5,190-->

25.确定列表长度？
?
len(cars)
<!--SR:!2025-04-01,12,270-->

26.使用for循环来打印魔术师名单中的所有名字：magicians = ['alice', 'david', 'carolina']
?
for magician in magicians:
print(magician)
<!--SR:!2025-04-02,10,273-->

27.写for循环时容易出错的两个点：
?
①循环内的语句没有缩进②忘记在for语句后面加冒号
<!--SR:!2025-04-05,12,274-->

28.用什么可以打印1~5（不包含5）?
?
for value in range(1,5):
	print(value)
<!--SR:!2025-03-28,5,234-->

29.将range打印出来的数字形成一个列表：
?
numbers=list(range(1,6))
print(numbers)
<!--SR:!2025-04-04,12,274-->

30.用函数range打印10以内的偶数，并转换成列表：
?
even_numbers = list(range(2,11,2))
print(even_numbers)
<!--SR:!2025-03-30,5,234-->

31.将前10个整数的平方一个一个加入到一个列表中：
?
squares = []
for value in range(1,11):
square = value **  2
squares.append(square)
print(squares)
或者：squares.append(value ** 2)
<!--SR:!2025-03-30,7,254-->

32.找出digits列表中的最大值、最小值、总和：
?
max(digits)
min(digits)
sum(digits)
<!--SR:!2025-04-04,11,274-->

33.用列表解析将前10个整数的平方一个一个加入到一个列表中：
?
squares = [value**2 for value in range(1,11)]
print(squares)
<!--SR:!2025-03-30,7,254-->

34.players = ['charles', 'martina', 'michael', 'florence', 'eli']只打印列表前三个元素、2~4个元素：
?
print(players[0:3])、print(players[1:4])
<!--SR:!2025-03-27,1,214-->

35.print(players[:4])表示？print(players[2:])呢
?
从列表开头开始，打印至第四个元素(即索引3）；从索引2开始打印至列表的最后一个元素
<!--SR:!2025-03-30,5,234-->

36.输出名单上的最后三名队员？
?
可使用切片players[-3:]
<!--SR:!2025-04-03,11,274-->

37.![[Pasted image 20250318162218.png]]和![[Pasted image 20250318162248.png]]
的区别
?
第二个的语法实际上是让Python将新变量friend_foods关联到包含在my_foods中的列表，因此这两个变量都指向同一个列表，输出是第一个符合要求，而第二个不符合
<!--SR:!2025-04-02,10,274-->

38.如果需要存储的一组值在程序的整个生命周期内都不变，可使用？怎么使用
?
可以使用元组；比如一个矩形的长和宽固定不变：dimensions=(40,200)；注意要使用圆括号
<!--SR:!2025-04-02,10,274-->

39.元组可以进行重新赋值吗？对单个元素进行索引修改呢？
?
可以；不可以
<!--SR:!2025-04-05,12,274-->

40.要判断特定的值是否已包含在列表中，可使用关键字
?
in
<!--SR:!2025-04-03,11,274-->

41.确定特定的值未包含在列表中很重要；在这种情况下，可使用关键字
?
not in。
<!--SR:!2025-04-02,10,274-->

42.将列表里的字符都进行lower处理：
?
curren_users=['Alice','wait','JOHN']
current.users=[u.lower() for u in current_users]
<!--SR:!2025-04-04,11,276-->

43.写一个包含外星人颜色和分数的字典，并且打印出每个键对应的值和打印整个字典出来：
?
alien_0 = {'color': 'green','points':5}
print(alien_0['color'])
print(alien_0['points'])
print(alien_0)
<!--SR:!2025-03-31,5,236-->

44.在字典alien_0中添加两项信息：外星人的x坐标和y坐标
?
alien_0['x_position'] = 0
alien_0['y_position'] = 25
<!--SR:!2025-04-05,12,276-->

45.创建一个空字典
?
alien_0 = {}
<!--SR:!2025-04-03,10,276-->

46.将字典中的一个外星人从绿色改为黄色：
?
alien['color']='yellow'
<!--SR:!2025-04-05,12,276-->

47.从字典alien_0中删除键'points'及其值：
?
del alien_0['points']
<!--SR:!2025-03-31,7,256-->

48.如何遍历字典中的所有键值对？有哪三个重要的构成？
?
for key, value in user_0.items():
<!--SR:!2025-04-03,10,276-->

49.如何遍历字典中所有的键？
?
for key in user_0.keys()
<!--SR:!2025-04-02,7,256-->

50.如何遍历字典中所有的值？
?
for value in user_0.values()
<!--SR:!2025-04-05,12,276-->

51.如何对字典中的键按字母顺序排列输出
?
for name in sorted(favorite_languages.keys()):
print(name.title() + ", thank you for taking the poll.")
<!--SR:!2025-03-29,3,216-->

52.如何对字典中的值精简输出，不重复：
?
for language in set(favorite_languages.values()):
print(language.title())
<!--SR:!2025-03-31,7,256-->

53.TypeError: 'int' object is not iterable什么意思？
?
指python
num = 5
for i in num:  # 错误！int 不可迭代
    print(i)
<!--SR:!2025-04-06,12,276-->

54.列表中存储字典,并且打印出来：
?
alien_0 = {'color': 'green', 'points': 5}
alien_1 = {'color': 'yellow', 'points': 10}
alien_2 = {'color': 'red', 'points': 15}
aliens = [alien_0, alien_1, alien_2]
for alien in aliens:
print(alien)
<!--SR:!2025-03-27,3,236-->

55.在字典pizza中存储toppings列表,并且打印出来：
?
pizza = {
  'crust': 'thick',
  'toppings': ['mushrooms', 'extra cheese'],
  }
for topping in pizza[[['toppings' ]]]:
print("\t" + topping)
<!--SR:!2025-03-30,4,216-->

56.字典中的items()只是返回：
?
key和value两个类型值，是键值对的形式，不是有多少个键值对
<!--SR:!2025-04-06,12,276-->

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
<!--SR:!2025-03-28,2,216-->

58.input的用法？比如让用户输入姓名？
?
name=input("Please enter your name: ")
print=("Hello, "+name+"!")
<!--SR:!2025-03-27,4,276-->

59.除了name=input("Please enter your name: ")，还有?多行的提示输入怎么弄？
?
prompt = "If you tell us who you are, we can personalize the messages you see."
prompt += "\nWhat is your first name? "
name=input(prompt)
<!--SR:!2025-04-06,11,276-->

60.使用函数input时，python将用户输入解读为？
?
字符串
<!--SR:!2025-03-27,3,256-->

61.将用户输入的字符串转换成数值,以方便进行数值上的条件比较：
?
age=int(age)
<!--SR:!2025-04-07,12,276-->

62.在要求很多条件都满足才继续运行的程序中，可定义一个变量，用于判断整个程序是否处于活动状态。这个变量被称为?
?
active,标志，当active=True时，循环继续进行，当为False时结束循环
<!--SR:!2025-03-27,4,276-->

63.什么让Python忽略余下的代码，并返回到循环的开头
?
continue
<!--SR:!2025-04-07,12,276-->

64.如果程序陷入无限循环，可按____或者____
?
Ctrl+C或者直接关闭终端窗口
<!--SR:!2025-03-27,4,276-->

65.创建一个不为空一个为空的列表，然后将这个列表迁移至另一个空列表如果迁移未结束则进行循环的while后面跟的条件是什么？
?
unconfirmed_users = ['alice', 'brian', 'candace']
confirmed_users = []
while unconfirmed_users:
<!--SR:!2025-04-07,12,276-->

66.用while删除列表里某一个值（重复的值）：pets=['dog', 'cat', 'dog', 'goldfish', 'cat', 'rabbit', 'cat']
?
while 'cat' in pets:
pets.remove('cat')
<!--SR:!2025-03-27,4,276-->

67.在while循环中怎么将用户输入的信息存储在一个字典中？
?
name = input("\nWhat is your name? ")
response = input("Which mountain would you like to climb someday? ")
responses[name] = response
<!--SR:!2025-03-27,3,256-->

68.进行问卷调查时怎么结束调查？
?
repeat = input("Would you like to let another person respond? (yes/ no) ")
if repeat == 'no':
polling_active = False#在前面定义
<!--SR:!2025-03-28,2,236-->

69.当调查结束时，为了显示调查结果而写的提示信息：
?
print("\n--- Poll Results ---")
<!--SR:!2025-03-27,3,256-->

70.TabError: inconsistent use of tabs and spaces in indentation
?
是缩进的错误，混用了空格和制表符
<!--SR:!2025-03-28,4,278-->

71.可使用什么关键字来告诉Python你要定义一个函数
?
def
<!--SR:!2025-03-28,3,261-->

72.在哪里描述函数是做什么的，用什么进行注释？
?
在def紧接着的下面一行，用“”“ ”“”叫文档字符串
<!--SR:!2025-03-29,4,282-->

73.实参是什么？
?
调用函数时传递给函数的信息
<!--SR:!2025-03-28,3,262-->

74.在传递实参时，字符要用什么包裹？
?
引号
<!--SR:!2025-03-28,3,262-->

75.使用位置实参来调用函数时，要注意：
?
确认函数调用中实参的顺序和函数定义中形参的顺序一致
<!--SR:!2025-03-29,3,262-->

76.关键字实参是什么
?
是传递给函数的名称-值 对，如describe_pet(animal_type='hamster', pet_name='harry')
<!--SR:!2025-03-28,3,262-->

77.使用关键字实参时，顺序重要吗？
?
不重要；这两个是等效的：describe_pet(animal_type='hamster', pet_name='harry')
describe_pet(pet_name='harry', animal_type='hamster')
<!--SR:!2025-03-28,3,261-->

78.如果没有显式地给形参提供实参，那么？
?
将使用函数定义时所设定地形参默认值
<!--SR:!2025-03-28,3,262-->

79.使用形参默认值时，在形参列表中必须先列出？后列出？
?
先列出没有默认值的形参，后列出有默认值的实参
<!--SR:!2025-03-28,3,261-->

80.函数除了能够直接用print显示输出，还能
?
使用return返回值、字典、列表
<!--SR:!2025-03-28,3,262-->

81.并不是所有人都有中间名，那么为了让传入的实参变成可选的，可以？这时候函数该怎么定义？所以有两个情况，为空和不为空，if判断的条件怎么写？
?
可给实参middle_name指定一个默认值——空字符串，且要将其移到末尾；def get_formatted_name(first_name, last_name, middle_name=''):
因为Python将非空字符串解读为True，所以
if middle_name:
full_name = first_name + ' ' + middle_name + ' ' + last_name
else:
full_name = first_name + ' ' + last_name
return full_name.title()
<!--SR:!2025-03-28,3,262-->

82.函数怎么返回字典？
?
直接return+字典名
<!--SR:!2025-03-28,3,261-->

83.如果遇到while循环条件是True，要怎么设计退出？
?
当满足一定条件后使用break,所以要提前告诉用户可以退出的办法，在循环内使用if进行条件判断，如果符合那么break
<!--SR:!2025-03-28,2,242-->

84.函数怎么传递列表？
?
直接函数名(列表名)
<!--SR:!2025-03-29,3,262-->

85.将列表传递给函数后，函数对其修改，这些修改都是？
?
永久性的
<!--SR:!2025-03-28,3,262-->

86.不修改原本的列表，可以使用
?
列表的副本，传递列表的副本func(list_name[:])
<!--SR:!2025-03-28,3,261-->

87.怎么传递任意数量的实参？
?
def make_pizza(*  toppings):形参名* toppings中的星号让Python创建一个名为toppings的空元组，并将收到的所有值都封装到这个元组中。(注意星号和形参之间没有空格，只是obsidian的格式问题)
<!--SR:!2025-03-29,3,261-->

88.怎么传递任意数量的关键字实参？
?
def build_profile(first, last, ** user_info):(注意星号和形参之间没有空格，只是obsidian的格式问题)形参** user_info中的两个星号让Python创建一个名为user_info的空字典，并将收到的所有名称—值对都封装到这个字典中。在这个函数中，可以像访问其他字典那样访问user_info中的名称—值对。
<!--SR:!2025-03-28,3,261-->

89.这些导入函数或模块的方法，分别该怎么调用函数？
import module_name
from module_name import function_name
from module_name import function_name as fn
import module_name as mn
from module_name import *
?
module_name.function()
function()
fn()
mn.function()
function()
<!--SR:!2025-03-28,3,261-->

90.在Python中，首字母大写的名称指的是？
?
类

91.class Dog():这个类定义中的括号是空的，说明？
?
没有继承任何类，是从空白开始创建这个类

92.创建类时，第一个要写的方法是？必不可少的形参是？
?
def __ init __ (self,name,age),self是必不可少的形参，还必须位于其他形参前面

93.怎么初始化属性：def __ init __ (self,name,age)
?
self.name = name
self.age = age

94.除了initi这个方法之外，在写其他方法时，必不可少的形参是？
?
self

95.我们通常可以认为首字母大写的名称（如
Dog）指的是类，而小写的名称（如my_dog）指的是?
?
根据类创建的实例

96.创建了实例my_dog之后该怎么访问属性？self.name = name
self.age = age
?
用句点表示法来获取属性，比如：my_dog.name

97.创建了实例my_dog之后该怎么调用方法？
?
my_dog.roll_over()

98.如果在方法init中添加了一个新属性，并且设置了初始值，如self.odometer_reading = 0，那么？
?
不需要提供形参

99.怎么修改属性的值?
?
①my_new_car.odometer_reading = 23
②通过方法修改：def update_odometer(self, mileage):
"""将里程表读数设置为指定的值"""
self.odometer_reading = mileage
my_new_car.update_odometer(23)

100.class ElectricCar(Car):创建子类时，在init方法中def __ init __ (self, make, model, year):首先要：
?
初始化父类的属性：super().__ init __ (make, model, year)

101.如果我们在子类中添加了新的属性，根据子类创建的实例中会有吗？父类呢？
?
子类会有，但是父类不会有

102.当调用子类创建实例时，如果用的是和父类中一样的方法，那么？
?
Python只关注子类中定义的

103.如果创建了类Battery,要怎么在类ElectricCar中将属性设置为该类？即根据这个类来创建实例，并把这个实例当作属性
?
self.battery = Battery()

104.将实例当作属性之后self.battery = Battery()要怎么调用方法Battery中的方法？
?
my_tesla.battery.describe_battery()

105.怎么导入模块（其实就是一个文件）中的类？
?
from car import Car

106.怎么从一个模块中导入多个类？
?
from car import Car, ElectricCar

107.怎么导入整个模块？
?
from car import Car, ElectricCar

108.from module_name import * 这是什么意思？
?

109.怎么创建一个有序的字典？
?
favorite_languages = OrderedDict()
favorite_languages['jen'] = 'python'
favorite_languages['sarah'] = 'c'
favorite_languages['edward'] = 'ruby'
favorite_languages['phil'] = 'python'

110.生成随机数的函数在什么模块里？
?
random

111.random模块里有一个函数可以返回一个位于指定范围的整数，该函数是什么，该怎么使用该函数进行随机数生成？
?
from random import randint
x = randint(1, 6)

112.在类中，可以用几个空行分隔方法？
?
一个

113.在模块中，可以用几个空行分隔类？
?
两个

114.在导入模块时，顺序一般是？两种模块之间该怎么区分？
?
先编写导入标准库模块的import语句，再添加一个空行，然后编写导入你自己编写的模块的import语句

115.UnicodeDecodeError: 'gbk' codec can't decode byte 0x9d in position 1856: illegal multibyte sequence这是什么错误？该怎么解决？
?
```python
with open('somefile.txt', encoding='utf-8') as f_object:
    contents = f_object.read()
print(contents)
```

116.