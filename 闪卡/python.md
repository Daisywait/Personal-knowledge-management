#python
1.在命令行运行python文件
?
python hello_world.py
<!--SR:!2025-05-17,43,290-->

2.变量名只能包含？且什么可以打头？
?
字母、下划线、数字；字母、下划线，数字不可以
<!--SR:!2025-05-01,30,270-->

3.字符串用什么包裹？
?
单引号和双引号都行，而且可以互相嵌套，比如：“  ‘ ’  ”；‘  “ ”  ’
<!--SR:!2025-05-19,45,290-->

4.name="anne waitwhat"对名字字符串进行首字母大写打印；还有全部大写或全部小写
?
print(name.title())；print(name.upper())、print(name.lower())
<!--SR:!2025-04-29,18,270-->

5.用什么来拼接字符串？
?
加号+
<!--SR:!2025-05-20,45,290-->

6.在字符串中添加制表符（tab）和换行符
?
\t \n
<!--SR:!2025-05-14,40,290-->

7.删除字符串末尾多余的后面？开头？同时？
?
favorite_language = ' python '
favorite_language.rstrip()
' python'
favorite_language.lstrip()
'python '
favorite_language.strip()
'python'
<!--SR:!2025-04-15,17,250-->

8.使用什么表示乘方运算
?
两个乘号，比如3**2 -表示3的二次方得9-
<!--SR:!2025-05-21,46,290-->

9.使用什么将非字符串转换成字符串？
?
str
<!--SR:!2025-05-15,41,290-->

10.用一个列表包含几种自行车
?
bicycles = ['trek', 'cannondale', 'redline', 'specialized']
<!--SR:!2025-05-01,30,270-->

11.返回列表中的最后一个元素、倒数第二个：
?
索引为-1、-2
<!--SR:!2025-05-18,44,290-->

12.将ducati元素附加到motorcycles列表末尾
?
append;
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)
motorcycles.append('ducati')
<!--SR:!2025-04-27,26,270-->

13.使用方法__可在motorcycles列表的任何位置添加新元素。为此，你需要指定__和__。motorcycles = ['honda', 'yamaha', 'suzuki']
?
motorcycles.insert(0, 'ducati')
print(motorcycles)
['ducati', 'honda', 'yamaha', 'suzuki']
<!--SR:!2025-05-03,22,230-->

14.如果知道要删除的元素在motorcycles列表中的位置，并且这个元素之后不再使用，可使用__语句来删除列表中的元素
?
motorcycles = ['honda', 'yamaha', 'suzuki']
print(motorcycles)
del motorcycles[0]
print(motorcycles)
['honda', 'yamaha', 'suzuki']
['yamaha', 'suzuki']
<!--SR:!2025-04-14,18,270-->

15.删除列表末尾的值，但是后期还需要使用它:motorcycles = ['honda', 'yamaha', 'suzuki']
?
popped_motorcycle = motorcycles.pop()
print(motorcycles)
print(popped_motorcycle)
<!--SR:!2025-04-16,18,250-->

16.想使用pop()删除列表中任何位置的元素：
?
first_owned = motorcycles.pop(0)
print('The first motorcycle I owned was a ' + first_owned.title() + '.')
<!--SR:!2025-04-29,28,270-->

17.如果知道要删除的值是什么，那么可以用
?
remove
motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati']
print(motorcycles)
motorcycles.remove('ducati')
print(motorcycles)
['honda', 'yamaha', 'suzuki', 'ducati']
['honda', 'yamaha', 'suzuki']
<!--SR:!2025-04-20,22,250-->

18.remove根据值删除了之后还可以后续使用这个值是因为：
?
可以把删除的原因存储到一个变量里，例如：
too_expensive = 'ducati'
motorcycles.remove(too_expensive)
print(motorcycles)
print("\nA " + too_expensive.title() + " is too expensive for me.")
<!--SR:!2025-04-16,18,250-->

19.SyntaxError: Non-UTF-8 code starting with '\xb4' in file D:\wait_what\Documents\python_work\python\Chapter03\list_2.py on line 2, but no encoding declared; see https://peps.python.org/pep-0263/ for details
?
要在第一行添加：# coding=utf-8
<!--SR:!2025-04-16,6,210-->

20.对列表内的元素进行字母顺序排列，这种排序方式有什么特点？
?
cars = ['bmw', 'audi', 'toyota', 'subaru']
cars.sort()
永久改变列表顺序
<!--SR:!2025-04-28,27,270-->

21.对列表内的元素进行字母逆序排列
?
cars.sort(reverse=True)
<!--SR:!2025-05-02,31,270-->

22.字母顺序临时排序
?
cars = ['bmw', 'audi', 'toyota', 'subaru']
sorted(cars)
<!--SR:!2025-04-30,29,270-->

23.字母逆序临时排序
?
cars = ['bmw', 'audi', 'toyota', 'subaru']
print(sorted(cars,reverse=True))
<!--SR:!2025-04-21,25,270-->

24.反转列表的排列顺序，有何特点？（不用sort)
?
cars.reverse(),永久性，但是再调用一次即可恢复
<!--SR:!2025-05-01,21,190-->

25.确定列表长度？
?
len(cars)
<!--SR:!2025-05-03,32,270-->

26.使用for循环来打印魔术师名单中的所有名字：magicians = ['alice', 'david', 'carolina']
?
for magician in magicians:
print(magician)
<!--SR:!2025-04-30,28,273-->

27.写for循环时容易出错的两个点：
?
①循环内的语句没有缩进②忘记在for语句后面加冒号
<!--SR:!2025-05-09,34,274-->

28.用什么可以打印1~5（不包含5）?
?
for value in range(1,5):
	print(value)
<!--SR:!2025-04-21,14,214-->

29.将range打印出来的数字形成一个列表：
?
numbers=list(range(1,6))
print(numbers)
<!--SR:!2025-05-07,33,274-->

30.用函数range打印10以内的偶数，并转换成列表：
?
even_numbers = list(range(2,11,2))
print(even_numbers)
<!--SR:!2025-04-14,13,234-->

31.将前10个整数的平方一个一个加入到一个列表中：
?
squares = []
for value in range(1,11):
square = value **  2
squares.append(square)
print(squares)
或者：squares.append(value ** 2)
<!--SR:!2025-04-20,19,254-->

32.找出digits列表中的最大值、最小值、总和：
?
max(digits)
min(digits)
sum(digits)
<!--SR:!2025-05-04,30,274-->

33.用列表解析将前10个整数的平方一个一个加入到一个列表中：
?
squares = [value**2 for value in range(1,11)]
print(squares)
<!--SR:!2025-04-15,10,234-->

34.players = ['charles', 'martina', 'michael', 'florence', 'eli']只打印列表前三个元素、2~4个元素：
?
print(players[0:3])、print(players[1:4])
<!--SR:!2025-04-25,17,234-->

35.print(players[:4])表示？print(players[2:])呢
?
从列表开头开始，打印至第四个元素(即索引3）；从索引2开始打印至列表的最后一个元素
<!--SR:!2025-04-14,13,234-->

36.输出名单上的最后三名队员？
?
可使用切片players[-3:]
<!--SR:!2025-05-05,31,274-->

37.![[Pasted image 20250318162218.png]]和![[Pasted image 20250318162248.png]]
的区别
?
第二个的语法实际上是让Python将新变量friend_foods关联到包含在my_foods中的列表，因此这两个变量都指向同一个列表，输出是第一个符合要求，而第二个不符合
<!--SR:!2025-04-28,26,274-->

38.如果需要存储的一组值在程序的整个生命周期内都不变，可使用？怎么使用
?
可以使用元组；比如一个矩形的长和宽固定不变：dimensions=(40,200)；注意要使用圆括号
<!--SR:!2025-04-29,27,274-->

39.元组可以进行重新赋值吗？对单个元素进行索引修改呢？
?
可以；不可以
<!--SR:!2025-05-08,33,274-->

40.要判断特定的值是否已包含在列表中，可使用关键字
?
in
<!--SR:!2025-05-05,31,274-->

41.确定特定的值未包含在列表中很重要；在这种情况下，可使用关键字
?
not in。
<!--SR:!2025-04-29,27,274-->

42.将列表里的字符都进行lower处理：
?
curren_users=['Alice','wait','JOHN']
current.users=[u.lower() for u in current_users]
<!--SR:!2025-05-04,30,276-->

43.写一个包含外星人颜色和分数的字典，并且打印出每个键对应的值和打印整个字典出来：
?
alien_0 = {'color': 'green','points':5}
print(alien_0['color'])
print(alien_0['points'])
print(alien_0)
<!--SR:!2025-04-14,13,236-->

44.在字典alien_0中添加两项信息：外星人的x坐标和y坐标
?
alien_0['x_position'] = 0
alien_0['y_position'] = 25
<!--SR:!2025-04-14,3,236-->

45.创建一个空字典
?
alien_0 = {}
<!--SR:!2025-05-02,28,276-->

46.将字典中的一个外星人从绿色改为黄色：
?
alien['color']='yellow'
<!--SR:!2025-05-08,33,276-->

47.从字典alien_0中删除键'points'及其值：
?
del alien_0['points']
<!--SR:!2025-04-19,18,256-->

48.如何遍历字典中的所有键值对？有哪三个重要的构成？
?
for key, value in user_0.items():
<!--SR:!2025-05-03,29,276-->

49.如何遍历字典中所有的键？
?
for key in user_0.keys()
<!--SR:!2025-04-21,19,256-->

50.如何遍历字典中所有的值？
?
for value in user_0.values()
<!--SR:!2025-05-07,32,276-->

51.如何对字典中的键按字母顺序排列输出
?
for name in sorted(favorite_languages.keys()):
print(name.title() + ", thank you for taking the poll.")
<!--SR:!2025-04-17,13,216-->

52.如何对字典中的值精简输出，不重复：
?
for language in set(favorite_languages.values()):
print(language.title())
<!--SR:!2025-04-18,17,256-->

53.TypeError: 'int' object is not iterable什么意思？
?
指python
num = 5
for i in num:  # 错误！int 不可迭代
    print(i)
<!--SR:!2025-05-10,34,276-->

54.列表中存储字典,并且打印出来：
?
alien_0 = {'color': 'green', 'points': 5}
alien_1 = {'color': 'yellow', 'points': 10}
alien_2 = {'color': 'red', 'points': 15}
aliens = [alien_0, alien_1, alien_2]
for alien in aliens:
print(alien)
<!--SR:!2025-04-15,13,236-->

55.在字典pizza中存储toppings列表,并且打印出来：
?
pizza = {
  'crust': 'thick',
  'toppings': ['mushrooms', 'extra cheese'],
  }
for topping in pizza[[['toppings' ]]]:
print("\t" + topping)
<!--SR:!2025-04-16,5,196-->

56.字典中的items()只是返回：
?
key和value两个类型值，是键值对的形式，不是有多少个键值对
<!--SR:!2025-05-09,33,276-->

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
<!--SR:!2025-04-16,5,196-->

58.input的用法？比如让用户输入姓名？
?
name=input("Please enter your name: ")
print=("Hello, "+name+"!")
<!--SR:!2025-05-24,43,296-->

59.除了name=input("Please enter your name: ")，还有?多行的提示输入怎么弄？
?
prompt = "If you tell us who you are, we can personalize the messages you see."
prompt += "\nWhat is your first name? "
name=input(prompt)
<!--SR:!2025-05-06,30,276-->

60.使用函数input时，python将用户输入解读为？
?
字符串
<!--SR:!2025-05-12,34,276-->

61.将用户输入的字符串转换成数值,以方便进行数值上的条件比较：
?
age=int(age)
<!--SR:!2025-05-11,34,276-->

62.在要求很多条件都满足才继续运行的程序中，可定义一个变量，用于判断整个程序是否处于活动状态。这个变量被称为?
?
active,标志，当active=True时，循环继续进行，当为False时结束循环
<!--SR:!2025-04-24,19,276-->

63.什么让Python忽略余下的代码，并返回到循环的开头
?
continue
<!--SR:!2025-05-11,34,276-->

64.如果程序陷入无限循环，可按____或者____
?
Ctrl+C或者直接关闭终端窗口
<!--SR:!2025-05-25,44,296-->

65.创建一个不为空一个为空的列表，然后将这个列表迁移至另一个空列表如果迁移未结束则进行循环的while后面跟的条件是什么？
?
unconfirmed_users = ['alice', 'brian', 'candace']
confirmed_users = []
while unconfirmed_users:
<!--SR:!2025-05-10,33,276-->

66.用while删除列表里某一个值（重复的值）：pets=['dog', 'cat', 'dog', 'goldfish', 'cat', 'rabbit', 'cat']
?
while 'cat' in pets:
pets.remove('cat')
<!--SR:!2025-05-11,33,276-->

67.在while循环中怎么将用户输入的信息存储在一个字典中？
?
name = input("\nWhat is your name? ")
response = input("Which mountain would you like to climb someday? ")
responses[name] = response
<!--SR:!2025-04-24,20,256-->

68.进行问卷调查时怎么结束调查？
?
repeat = input("Would you like to let another person respond? (yes/ no) ")
if repeat == 'no':
polling_active = False#在前面定义
<!--SR:!2025-04-15,13,236-->

69.当调查结束时，为了显示调查结果而写的提示信息：
?
print("\n--- Poll Results ---")
<!--SR:!2025-05-12,34,276-->

70.TabError: inconsistent use of tabs and spaces in indentation
?
是缩进的错误，混用了空格和制表符
<!--SR:!2025-05-13,33,278-->

71.可使用什么关键字来告诉Python你要定义一个函数
?
def
<!--SR:!2025-05-15,35,281-->

72.在哪里描述函数是做什么的，用什么进行注释？
?
在def紧接着的下面一行，用“”“ ”“”叫文档字符串
<!--SR:!2025-04-13,15,302-->

73.实参是什么？
?
调用函数时传递给函数的信息
<!--SR:!2025-05-14,34,282-->

74.在传递实参时，字符要用什么包裹？
?
引号
<!--SR:!2025-05-08,30,282-->

75.使用位置实参来调用函数时，要注意：
?
确认函数调用中实参的顺序和函数定义中形参的顺序一致
<!--SR:!2025-05-01,24,262-->

76.关键字实参是什么
?
是传递给函数的名称-值 对，如describe_pet(animal_type='hamster', pet_name='harry')
<!--SR:!2025-05-06,29,282-->

77.使用关键字实参时，顺序重要吗？
?
不重要；这两个是等效的：describe_pet(animal_type='hamster', pet_name='harry')
describe_pet(pet_name='harry', animal_type='hamster')
<!--SR:!2025-05-05,28,281-->

78.如果没有显式地给形参提供实参，而且函数有形参默认值时，那么？
?
将使用函数定义时所设定的形参默认值
<!--SR:!2025-04-14,3,222-->

79.使用形参默认值时，在形参列表中必须先列出？后列出？
?
先列出没有默认值的形参，后列出有默认值的实参
<!--SR:!2025-05-09,31,281-->

80.函数除了能够直接用print显示输出，还能
?
使用return返回值、字典、列表
<!--SR:!2025-05-13,33,282-->

81.并不是所有人都有中间名，那么为了让传入的实参变成可选的，可以？这时候函数该怎么定义？所以有两个情况，为空和不为空，if判断的条件怎么写？
?
可给实参middle_name指定一个默认值——空字符串，且要将其移到末尾；def get_formatted_name(first_name, last_name, middle_name=''):
因为Python将非空字符串解读为True，所以
if middle_name:
full_name = first_name + ' ' + middle_name + ' ' + last_name
else:
full_name = first_name + ' ' + last_name
return full_name.title()
<!--SR:!2025-04-21,11,242-->

82.函数怎么返回字典？
?
直接return+字典名
<!--SR:!2025-04-26,21,261-->

83.如果遇到while循环条件是True，要怎么设计退出？
?
当满足一定条件后使用break,所以要提前告诉用户可以退出的办法，在循环内使用if进行条件判断，如果符合那么break
<!--SR:!2025-04-23,19,262-->

84.函数怎么传递列表？
?
直接函数名(列表名)
<!--SR:!2025-05-02,25,262-->

85.将列表传递给函数后，函数对其修改，这些修改都是？
?
永久性的
<!--SR:!2025-05-10,32,282-->

86.不修改原本的列表，可以使用
?
列表的副本，传递列表的副本func(list_name[:])
<!--SR:!2025-04-28,22,261-->

87.怎么传递任意数量的实参？
?
def make_pizza(*  toppings):形参名* toppings中的星号让Python创建一个名为toppings的空元组，并将收到的所有值都封装到这个元组中。(注意星号和形参之间没有空格，只是obsidian的格式问题)
<!--SR:!2025-04-30,23,261-->

88.怎么传递任意数量的关键字实参？
?
def build_profile(first, last, ** user_info):(注意星号和形参之间没有空格，只是obsidian的格式问题)形参** user_info中的两个星号让Python创建一个名为user_info的空字典，并将收到的所有名称—值对都封装到这个字典中。在这个函数中，可以像访问其他字典那样访问user_info中的名称—值对。
<!--SR:!2025-04-17,11,241-->

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
<!--SR:!2025-04-16,6,261-->

90.在Python中，首字母大写的名称指的是？
?
类
<!--SR:!2025-04-12,11,283-->

91.class Dog():这个类定义中的括号是空的，说明？
?
没有继承任何类，是从空白开始创建这个类
<!--SR:!2025-04-30,20,264-->

92.创建类时，第一个要写的方法是？必不可少的形参是？并且位置一定要位于？
?
def __ init __ (self,name,age),self是必不可少的形参，还必须位于其他形参前面
<!--SR:!2025-05-09,28,284-->

93.怎么初始化属性：def __ init __ (self,name,age)
?
self.name = name
self.age = age
<!--SR:!2025-04-13,12,283-->

94.除了init这个方法之外，在写其他方法时，必不可少的形参是？
?
self
<!--SR:!2025-05-01,21,264-->

95.我们通常可以认为首字母大写的名称（如
Dog）指的是类，而小写的名称（如my_dog）指的是?
?
根据类创建的实例
<!--SR:!2025-05-04,24,265-->

96.创建了实例my_dog之后该怎么访问属性？self.name = name
self.age = age
?
用句点表示法来获取属性，比如：my_dog.name
<!--SR:!2025-05-01,21,265-->

97.创建了实例my_dog之后该怎么调用方法？
?
my_dog.roll_over()
<!--SR:!2025-04-13,12,283-->

98.如果在方法init中添加了一个新属性，并且设置了初始值，如self.odometer_reading = 0，那么？
?
不需要提供形参
<!--SR:!2025-05-04,24,265-->

99.怎么修改属性的值?(两种办法)
?
①my_new_car.odometer_reading = 23
②通过方法修改：def update_odometer(self, mileage):
"""将里程表读数设置为指定的值"""
self.odometer_reading = mileage
my_new_car.update_odometer(23)
<!--SR:!2025-04-19,13,245-->

100.class ElectricCar(Car):创建子类时，在init方法中def __ init __ (self, make, model, year):首先要：
?
初始化父类的属性：super().__ init __ (make, model, year)
<!--SR:!2025-04-16,6,205-->

101.如果我们在子类中添加了新的属性，根据子类创建的实例中会有吗？父类呢？
?
子类会有，但是父类不会有
<!--SR:!2025-05-02,22,265-->

102.当调用子类创建实例时，如果用的是和父类中一样的方法，那么？
?
Python只关注子类中定义的
<!--SR:!2025-04-12,11,284-->

103.如果创建了类Battery,要怎么在类ElectricCar中将属性设置为该类？即根据这个类来创建实例，并把这个实例当作属性
?
self.battery = Battery()
<!--SR:!2025-05-08,27,283-->

104.将实例当作属性之后self.battery = Battery()要怎么调用方法Battery中的方法？
?
my_tesla = ElectricCar('tesla', 'model s', 2016)
my_tesla.battery.describe_battery()
<!--SR:!2025-05-04,24,265-->

105.怎么导入模块（其实就是一个文件）中的类？
?
from car import Car
<!--SR:!2025-05-02,22,264-->

106.怎么从一个模块中导入多个类？
?
from car import Car, ElectricCar
<!--SR:!2025-04-27,19,265-->

107.怎么导入整个模块？
?
import module_name
<!--SR:!2025-05-05,25,264-->

108.from module_name import * 这是什么意思？
?
要导入模块中的每个类
<!--SR:!2025-05-05,25,263-->

109.怎么创建一个有序的字典？
?
favorite_languages = OrderedDict()
favorite_languages['jen'] = 'python'
favorite_languages['sarah'] = 'c'
favorite_languages['edward'] = 'ruby'
favorite_languages['phil'] = 'python'
<!--SR:!2025-04-22,12,245-->

110.生成随机数的函数在什么模块里？
?
random
<!--SR:!2025-04-13,12,283-->

111.random模块里有一个函数可以返回一个位于指定范围的整数，该函数是什么，该怎么使用该函数进行随机数生成？
?
from random import randint
x = randint(1, 6)
<!--SR:!2025-04-25,17,244-->

112.在类中，可以用几个空行分隔方法？
?
一个
<!--SR:!2025-04-30,20,265-->

113.在模块中，可以用几个空行分隔类？
?
两个
<!--SR:!2025-04-12,4,243-->

114.在导入模块时，顺序一般是？两种模块之间该怎么区分？
?
先编写导入标准库模块的import语句，再添加一个空行，然后编写导入你自己编写的模块的import语句
<!--SR:!2025-04-13,12,283-->

115.UnicodeDecodeError: 'gbk' codec can't decode byte 0x9d in position 1856: illegal multibyte sequence这是什么错误？该怎么解决？
?
```python
with open('somefile.txt', encoding='utf-8') as f_object:
    contents = f_object.read()
print(contents)
```
<!--SR:!2025-04-13,2,165-->

116.打开文件pi_digits.txt，并且读取用什么方法？加上全部打印出来，而不是分行
?
with open('pi_digits.txt') as file_object:
contents = file_object.read()
print(contents)
<!--SR:!2025-04-15,5,244-->

117.关键字with在什么时候关闭所选文件？
?
不再需要访问文件后
<!--SR:!2025-05-09,28,284-->

118.read()到达文件末尾时会：
?
返回一个空字符串，即空行
<!--SR:!2025-04-12,11,284-->

119.当你将类似pi_digits.txt这样的简单文件名传递给函数open()时，python将在哪里查找这个文件？
?
Python将在当前执行的文件（即.py程序文件）所在的目录中查找文件。
<!--SR:!2025-04-13,12,284-->

120.要让Python打开不与程序文件位于同一个目录中的文件，需要？
?
需要提供文件路径，它让Python到系统的特定位置去查找
<!--SR:!2025-04-12,11,284-->

121.Windows系统中，在文件路径中什么斜杠？
?
使用反斜杠（\）而不是斜杠（/）
<!--SR:!2025-04-13,12,284-->

122.比如你写的程序文件在python_work中，而要读取的文件在python_work中的另一个文件夹text_files,那么此时相对路径是？
?
with open('text_files\filename.txt') as file_object:
<!--SR:!2025-05-03,23,264-->

123.绝对文件路径是什么？长什么样子？
?
file_path = 'C:\Users\ehmatthes\other_files\text_files\filename.txt
<!--SR:!2025-04-13,12,284-->

124.对写入了多行文本的文件进行每一行读取且打印：
?
filename = 'pi_digits.txt'
with open(filename) as file_object:
	for line in file_object:
	print(line)
<!--SR:!2025-04-16,8,204-->

125.如果要在with代码块外访问文件的内容，可？该怎么写？用什么方法？
?
在with代码块内将文件的各行存储在一个列表中，并在with代码块外使用该列表.
filename = 'pi_digits.txt'
with open(filename) as file_object:
	lines = file_object.readlines()
for line in lines:
print(line.rstrip())
<!--SR:!2025-04-18,12,244-->

126.读取文本文件时，Python将其中的所有文本都解读？如果你读取的是数字，并要将其作为数值使用，就必须使用函数？
?
字符串；int()将其转换为整数，或者float将其转换成浮点数
<!--SR:!2025-04-18,17,304-->

127.pi_string是存储了一百万位的圆周率字符串，只打印到小数点后50位怎么表示？
?
print(pi_string[:52])
<!--SR:!2025-04-22,12,264-->

128.输入一串数字字符串，检查是否在pi_string 里用的判断语句是？
?
if birthday in pi_string:
<!--SR:!2025-04-15,5,244-->

129.open函数提供了两个实参，分别是？
?
第一个实参也是要打开的文件的名称；第二个实参（'w'）告诉Python，我们要以写入模式打开这个文件。
<!--SR:!2025-04-12,11,284-->

130.想要写入文件/读取模式/附加模式/读取+写入可以怎么调用open函数？采取什么方法进行写入？
?
filename = 'programming.txt'
with open(filename, 'w') as file_object:
file_object.write("I love programming.")
读取模式（'r'）、写入模式（'w'）、附加模式（'a'）或让你能够读取和写入文件的模式（'r+'）
<!--SR:!2025-04-18,12,244-->

131.如果你要写入的文件不存在，函数open()将？
?
自动创建它。
<!--SR:!2025-05-10,29,284-->

132.然而，以写入（'w'）模式打开文件时千万要小心，因为如果指定的文件已经存在，Python将?
?
在返回文件对象前清空该文件。也就是覆盖了
<!--SR:!2025-04-13,12,284-->

133写入多行时，函数write会像print一样自动添加换行符吗？
?
不会
<!--SR:!2025-05-08,27,284-->

134.编写一个try-except代码块来处理理 ZeroDivisionError 异常？
?
try:
	print(5/0)
except ZeroDivisionError:
	print("You can't divide by zero!")
<!--SR:!2025-04-12,11,284-->

135.else代码块，用来存放？
?
依赖于try代码块成功执行的代码
<!--SR:!2025-04-12,11,284-->

136.除了ZeroDivisionError 异常还有？
?
FileNotFoundError 异常
<!--SR:!2025-04-23,13,264-->

137.方法split()是怎么起作用的？且该怎么调用它？
?
以空格为分隔符将字符串分拆成多个部分，并将这些部分都存储到一个列表中。结果是一个包含字符串中所有单词的列表，虽然有些单词可能包含标点。
text="I like reading, but she doesn't"
words=text.split()
print(words)
<!--SR:!2025-04-16,8,204-->

138.遇到异常时选择忽略：
?
except FileNotFoundError:
	pass
<!--SR:!2025-04-12,11,284-->

139.程序都把用户提供的信息存储在
?
列表和字典等数据结构中。
<!--SR:!2025-04-24,14,264-->

140.用什么模块来存储数据？
?
一种简单的方式是使用模块json来存储数据。
<!--SR:!2025-05-03,23,264-->

141.json全称？
?
JSON（JavaScript Object Notation）
<!--SR:!2025-04-13,12,284-->

142.将列表存储为json格式的文件？需要注意几点？
?
导入json模块，还有文件后缀，以及函数的调用格式
import json
numbers = [2, 3, 5, 7, 11, 13]
filename = 'numbers.json'
with open(filename, 'w') as f_obj:
	json.dump(numbers, f_obj)
<!--SR:!2025-04-12,2,164-->

143.将文件中的列表读入到内存中？用什么函数？
?
import json
filename = 'numbers.json'
with open(filename) as f_obj:
	numbers = json.load(f_obj)
print(numbers)
<!--SR:!2025-04-16,5,164-->

144.json是一种？
?
这是一种在程序之间共享数据的简单方式。除了python其他语言也在使用
<!--SR:!2025-04-17,11,244-->

145.检查字符串是否为空的判断条件？
?
if username:
  print("Welcome back, " + username + "!")
<!--SR:!2025-04-12,11,284-->

146.如果字符串长这样full_name = first + ' ' + last，first和last时传进去的实参，那么可以使用title函数吗？
?
可以，直接full_name.title()
<!--SR:!2025-04-14,9,265-->

147.Python标准库中的什么模块提供了代码测试工具？
?
模块unittest
<!--SR:!2025-04-23,12,245-->

148.对编写的函数进行测试用例编写时，需要导入什么？
?
一个是测试代码工具，即模块模块unittest，一个是将要被测试的函数
<!--SR:!2025-04-14,9,265-->

149.除了导入模块外，编写测试用例的步骤是什么？
?
创建一个类，这个类继承unittest的类unittest.TestCase，然后在类中定义一个方法，方法必须哦那个test开头(将会自动运行)，使用适当的断言进行测试，最后用unittest.main()使这个测试用例发挥作用
import unittest
from name_function import get_formatted_name
class NamesTestCase(unittest.TestCase):
"""测试name_function.py"""
	def test_first_last_name(self):
	"""能够正确地处理像Janis Joplin这样的姓名吗？"""
		formatted_name = get_formatted_name('janis', 'joplin')
		self.assertEqual(formatted_name, 'Janis Joplin')
unittest.main()
<!--SR:!2025-04-12,2,185-->


150.什么断言方法用来核实得到的结果是否与期望的结果一致？具体怎么使用
?
self.assertEqual(formatted_name, 'Janis Joplin')
<!--SR:!2025-04-12,5,225-->

152.在运行完测试用例之后，首行的句点代表的意思是？
?
表示测试通过，有几个句点就代表有几个测试通过了
<!--SR:!2025-04-14,9,265-->


153.![[Pasted image 20250401162557.png]]一一说出实现这些的断言方法是？
?
![[Pasted image 20250401162638.png]]
<!--SR:!2025-04-22,11,245-->

154.类的测试与函数的测试相似——所做的大部分工作都是测试？所以要？
?
类中方法的行为；要测试类的行为，需要创建其实例。
<!--SR:!2025-04-15,5,225-->

155.如果在不同的测试方法中都用到同样/相似的对象，那么？
?
可以使用方法setUp
def setUp(self):
"""
创建一个调查对象和一组答案，供使用的测试方法使用
"""
question = "What language did you first learn to speak?"
self.my_survey = AnonymousSurvey(question)
self.responses = ['English', 'Spanish', 'Mandarin']
<!--SR:!2025-04-12,5,245-->

156.测试通过时？；测试引发错误时?；测试导致断言失败时?
?
打印一个句点;打印一个E;打印一个F
<!--SR:!2025-04-22,11,245-->

157.在写外星人入侵项目源文件时即运行游戏的那个文件需要导入什么模块？
?
import sys来响应退出事件
import pygame来初始化游戏和设置游戏
<!--SR:!2025-04-12,5,225-->

158.在游戏程序开头需要在创建运行游戏函数后的第一步是？起到了什么作用
?
初始化pygame,即pygame.init()，![[Pasted image 20250401191327.png]]
<!--SR:!2025-04-23,12,245-->

159.用pygame的什么可以创建屏幕窗口？
?
screen=pygame.display.set_mode((1200,600))#设置窗口为1200，600
<!--SR:!2025-04-24,13,245-->

160.设置背景颜色，并呈现
?
bg_color=[255,0,0]
在循环中screen.fill(bg_color)
<!--SR:!2025-04-12,5,225-->

161设置窗口标题
?
pygame.display.set_caption("Alien Invasion")
<!--SR:!2025-04-23,12,245-->

162.在游戏主循环里，处理事件“退出”怎么写？
?
while True:
		for event in pygame.event.get():
			if event.type== pygame.QUIT:#如果点击事件为退出那么就调用sys的退出函数
				sys.exit()
<!--SR:!2025-04-12,5,225-->

163.更新屏幕显示？
?
pygame.display.flip()也是在主循环里实现的
<!--SR:!2025-04-24,13,245-->

164.选择用于表示飞船的图像后，需要将其显示到屏幕上。我们将创建一个名为ship的模块，其
中包含Ship类，它负责管理飞船的大部分行为，而这个类里要写几个方法？方法具体是实现了什么？
?
先导入pygame模块，然后编写类Ship；第一个是初始化init，里面包含导入图像，然后获取图像的外接矩形，还有飞船的放置位置；第二个方法是在屏幕上绘制飞船
<!--SR:!2025-04-16,9,264-->

165.加载飞船图像并获取其外接矩形：
?
self.image = pygame.image.load('images/ship.bmp')
self.rect = self.image.get_rect()
self.screen_rect = screen.get_rect()
<!--SR:!2025-04-14,4,224-->

166.将每艘新飞船放在屏幕底部中央？
?
self.rect.centerx = self.screen_rect.centerx
self.rect.bottom = self.screen_rect.bottom
<!--SR:!2025-04-12,5,244-->

167.在指定位置绘制飞船的方法（只是绘制，不是怎么绘制）
?
screen = pygame.display.set_mode((1200, 800))
在方法init中初始化：self.screen = screen
def blitme(self):
self.screen.blit(self.image, self.rect)
<!--SR:!2025-04-13,2,164-->

168.怎么确保让飞船在背景之后出现？
?
screen.fill(ai_settings.bg_color)
ship.blitme()
填充背景色之后再进行飞船的绘制
<!--SR:!2025-04-13,2,184-->

169.pip是？
?
 是一个负责为你下载并安装Python包的程序
<!--SR:!2025-04-13,3,260-->
 
170.pygame.display.flip()的作用是？
?
将不断更新屏幕，以显示元素的新位置，并在原来的位置隐藏元素，从而营造平滑移动的效果。
<!--SR:!2025-04-13,3,260-->

171.若不指定背景色，Pygame默认创建？
?
一个黑色屏幕
<!--SR:!2025-04-13,3,259-->

172.对于图片，Pygame默认加载？
?
位图(.bmp)。
<!--SR:!2025-04-13,3,260-->

173.要将游戏元素居中，可设置相应rect对象的属性: 要让游戏元素与屏幕边缘对齐，可使用属性:
 ?
 center、centerx或centery;top、bottom、left或right；
 self.rect.centerx = self.screen_rect.centerx
self.rect.bottom = self.screen_rect.bottom
<!--SR:!2025-04-12,1,220-->

174.在Pygame中，原点(0, 0)位于屏幕左上角，向右下方移动时，两个坐标值都怎么变化？在1200×800的屏幕上，原点位于？而右下角的坐标为？
?
都增大；(1200, 800)。
<!--SR:!2025-04-13,3,259-->

175.一开始将代码编写得尽可能？并在项目越来越复杂时进行?
?
简单;重构。
<!--SR:!2025-04-13,3,259-->

176.事件都是通过什么方法获取的？在函数check_events()中，我们需要指定要检查哪些类型的事件。每次按键都被注册为一个什么事件？
 ?
 方法pygame.event.get();KEYDOWN事件
<!--SR:!2025-04-13,2,240-->

177.rect的centerx等属性只能存储？那要怎么让speed_factor为小数时也发挥作用？
?
整数值；设置一个新的属性self.center，self.center = float(self.rect.centerx)，然后在更新飞船位置的时候直接更新self.center,self.center += self.ai_settings.ship_speed_factor，后面再更新rect值self.rect.centerx = self.center；self.rect.centerx将只存储self.center的整数部分，但对显示飞船而言，这问题不大。
<!--SR:!2025-04-13,3,260-->

178.为了防止飞船出屏幕，判断条件该怎么写？
?
if self.moving_up and self.rect.top>0:
self.centery-=self.ai_settings.ship_speed_factor
if self.moving_down and self.rect.bottom<self.screen_rect.bottom:
self.centery+=self.ai_settings.ship_speed_factor
if self.moving_right and self.rect.right<self.screen_rect.right:
self.centerx+=self.ai_settings.ship_speed_factor
if self.moving_left and self.rect.left>0:
self.centerx-=self.ai_settings.ship_speed_factor
<!--SR:!2025-04-13,2,240-->

179.将子弹颜色设置成深灰色：
?
self.bullet_color = 60, 60, 60
<!--SR:!2025-04-13,2,240-->

180.创建存储Bullet类的文件bullet.py时，需要导入什么模块？分别有何作用？
?
import pygame
from pygame.sprite import Sprite
第一个pygame模块是为了创建子弹外形self.rect = pygame.Rect(0, 0, ai_settings.bullet_width,
ai_settings.bullet_height)表示在(0,0)处进行创建ai_settings.bullet_width,ai_settings.bullet_height的子弹矩形；
第二个是Sprite类为了后面根据此类进行实例创建后，对子弹元素可以统一进行编组和管理
<!--SR:!2025-04-13,3,259-->

181.为了让子弹看起来是飞船发射的，子弹的位置怎么设置？
?
self.rect.centerx = ship.rect.centerx
self.rect.top = ship.rect.top
<!--SR:!2025-04-13,2,240-->

182.在bullet.py中创建方法，在屏幕上绘制子弹？
?
def draw_bullet(self):
"""在屏幕上绘制子弹"""
pygame.draw.rect(self.screen, self.color, self.rect)
<!--SR:!2025-04-12,1,220-->

183.创建一个用于存储子弹的编组需要导入什么模块？怎么创建？起到了什么作用，举一个调用方法的例子
?
from pygame.sprite import Group
bullets = Group()
bullets.update()
当你对编组调用update()时，编组将自动对其中的每个精灵调用update()，因此代码行bullets.update()将为编组bullets中的每颗子弹调用bullet.update()。bullet.update()是bullet.py文件里更新子弹位置的方法
<!--SR:!2025-04-12,1,219-->

184.在创建完子弹编组bullets = Group()之后，怎么实现按下空格键就发射子弹？逻辑上阐述
?
1.**根据事件检测新增子弹**
bullets = Group()#这是在循环之外创建的，实际上这是一个空的容器(功能另说)，检测到按下空格键事件之后，可以向编组里新增子弹：
elif event.key == pygame.K_SPACE:
  创建一颗子弹，并将其加入到编组bullets中
  new_bullet = Bullet(ai_settings, screen, ship) # 这个是新建每一个子弹实例
  bullets.add(new_bullet)#将新增的子弹实例添加精灵编组里
  2.**之后通过绘制显示新增的子弹**：
  在update_screen方法里
  for bullet in bullets.sprites(): # 方法bullets.sprites()返回一个列表，其中包含编组bullets中的所有精灵。
  bullet.draw_bullet()#调用类Bullet里面的方法进行绘制，为什么能调用？因为这个子弹其实是新增的，通过类Bullet创建的实例。
<!--SR:!2025-04-13,3,260-->
  
185.contents = file_object.read()和contents=json.load(file_object)有啥区别吗
?
![[Pasted image 20250410164252.png]]
read()返回的统统都是字符串
<!--SR:!2025-04-13,3,259-->

186.在方法update_screen里绘制子弹
?
for bullet in bullets.sprites():
  bullet.draw_bullet()
  为在屏幕上绘制发射的
 所有子弹，我们遍历编组bullets中的精灵，并对每个精灵都调用draw_bullet()
<!--SR:!2025-04-12,1,238-->
 
187.
![[Pasted image 20250411172708.png]]

