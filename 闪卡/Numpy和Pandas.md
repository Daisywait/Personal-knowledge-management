#numpy和pandas 
1.A = np.random.random((4, 4))是做了什么？
?
通过导入的库numpy、调用random模块中的random函数，生成4×4的二维矩阵，数组中的每个元素都是在 `[0.0, 1.0]`区间内的随机浮点数。

2.np.arange(4) 是？
?
NumPy 库中的一个函数调用，用于生成一个等间隔的数值序列，并将其存储为 NumPy 数组（ndarray 对象）。这里是start=0,step=1,生成到3，即`[0,1,2,3]`的等差一维numpy数组

3.np.arange 函数的语法？
?
numpy.arange(`[start,] stop[, step,], dtype=None`)
![[Pasted image 20250425103155.png]]

4.import numpy as np A = np.array(`[[1, 2], [3, 4]]`) B = np.array(`[[5, 6], [7, 8]]` print(A * B)结果是？
?
`[[5 12] [21 32]]`

5.import numpy as np
     A = np.array(`[[1, 2, 3], [4, 5, 6]]`)
     B = np.array(`[1, 2, 3]`)
     print(A * B)  结果是？
?
`[[1 4 9] [4 10 18]]`

6.numpy可以执行矩阵乘法的函数是？
?
print(np.dot(A, B)) # 直接调用库中的函数，传入两个数组A,B
print(A.dot(B)) # 使用数组对象的方法dot()

7.矩阵乘法的乘法规则是？
?
计算方法是将矩阵 A 的每一行与矩阵 B 的每一列对应元素相乘后求和。

8.```
```
import numpy as np
A = np.array([[1, 2], [0, 3]])
B = np.array([[2, 4], [5, 0]]) 
result = np.dot(A, B)
  print(result)
```
结果是？
?
`输出: [[12 4] [15 0]]`

9.A，B分别是2×3的二维数组，print(np.vstack((A, B)))、print(np.hstack((A, B)))分别实现了什么？
?
B会被放在A下方；B会被放在A右侧

10.a,b,c都是一维数组，print(np.column_stack((a, b, c)))和print(np.row_stack((a, b, c)))分别实现了什么？
?
输入是一维数组，它们会被转换为列向量，然后按列堆叠在一起。类似地，第二个是被转换成行向量然后按照行堆叠在一期

11.print(np.hsplit(A, 2))、.print(np.vsplit(A, 2))是实现了什么？
?
函数用于将数组 A 水平（列方向）分割成两个子数组。如果指定了一个整数 n，则数组会被分割成 n 个形状相同的子数组,这里指定2;第二个是行方向

12.使用`np.hsplit(arr, [1, 3])`会实现什么？
?
将数组在第1列和第3列之前进行分割。这意味着数组将被分割成三个部分：第一个部分包含第0列，第二个部分包含第1列和第2列，第三个部分包含第3列。

13.`print(np.split(A, [1, 3], axis=1))`会实现什么？
?
将数组在第1列和第3列之前进行分割。这意味着数组将被分割成三个部分：第一个部分包含第0列，第二个部分包含第1列和第2列，第三个部分包含第3列。axis表示列方向

14.写一个结构化数组，包含四个字段，第一个字段是整数，第二个是字符串，第三个是浮点数，第四个是负数，并且指定类型
?
```
structured = np.array(
  [(1, 'First', 0.5, 1+2j),
   (2, 'Second', 1.3, 2-2j),
   (3, 'Third', 0.8, 1+3j)],
  dtype=('i2, a6, f4, c8'))
```

15.
```
structured = np.array(
  [(1, 'First', 0.5, 1+2j),
   (2, 'Second', 1.3, 2-2j),
   (3, 'Third', 0.8, 1+3j)],
  dtype=('i2, a6, f4, c8'))
```
显式指定字段名称
?
```
structured = np.array(
  [(1, 'First', 0.5, 1+2j),
   (2, 'Second', 1.3, 2-2j),
   (3, 'Third', 0.8, 1+3j)],
  dtype=[('id', 'i2'), ('position', 'a6'), ('value', 'f4'), ('complex', 'c8')])
```

16.
```
structured = np.array(
  [(1, 'First', 0.5, 1+2j),
   (2, 'Second', 1.3, 2-2j),
   (3, 'Third', 0.8, 1+3j)],
  dtype=[('id', 'i2'), ('position', 'a6'), ('value', 'f4'), ('complex', 'c8')])
```
通过字段来访问数据？
?
```
print(structured['position'])
# 输出: [b'First' b'Second' b'Third']
```

17.
```
   a = np.array([1, 2, 3, 4])
```
怎么查看数组a的元素类型？且输出的元素类型是？
?
 print(a.dtype)  # 输出: int64

18.
```
   a = np.array([1, 2, 3, 'ab'])
   print(a.dtype)  输出？
```
?
` 输出: <U21`当数组中包含不同类型的数据时，NumPy 会将所有元素转换为一种通用类型。在这个例子中，所有元素都被转换为字符串类型 <U21，其中 <U 表示 Unicode 字符串，21 表示每个字符串的最大长度

19.显式指定数组a的数据类型为int32
?
```
   a = np.array([1, 2, 3], dtype=np.int32)
   print(a.dtype)  # 输出: int32
```

20.
```
   a = np.array([1, 2, 3.0])
   print(a.dtype)  
```
?
`# 输出: float64`

21.用什么属性来返回a数组中元素的总数？
?
a.size
```
  A = np.array([[1, 4], [9, 5]])
  print(A.shape)  # the shape of the array
  print(A.size)   # number of elements
```

22.
```
  a = np.array([1, 2, 3])
  print(a.shape) # (3,)
```
输出表示？
?
输出 (3,) 表示数组 a 是一个包含 3 个元素的一维数组。如果是一个2×3的二维数组则会输出（2，3）

23.怎么遍历二维数组A的每一行，并逐行打印出来？
?
for row in A: print(row)

24.深拷贝和浅拷贝数组a?两者之间有什么区别？
?
```
d = a.copy()#是两个独立的数组
print(d is a) #输出: False
print(d.base is a) #输出: False
b=a.view()#视图独立，比如b.shape=(3,1),但不会改变a的shape；并且指向的内存空间一致，即改变b就会改变a
print(c is a) #输出: False
print(c.base is a) #输出: True
```


25.深拷贝也可以用于DataFrame,`df = pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6]})`
?
df_copy = df.copy()

26.将DataFrame进行转置，转置是什么意思？
?
df.T，转置操作是指将 DataFrame 的行和列进行互换，即原来的行变为列，原来的列变为行。

27.np.apply_along_axis(np.mean, axis=0, arr=A)实现了什么?
?
这个函数调用的作用是对数组 A 的每一列计算平均值。
![[Pasted image 20250425114735.png]]

28.创建一个复数类型的数组？
?
```
f = np.array([[1, 2, 3], [4, 5, 6]], dtype=complex)
```

29.在NumPy中，默认的复数类型是 ?
?
complex128
这意味着每个复数由两个64位浮点数组成（实部和虚部各一个64位浮点数）。

30
```
f = np.array([[1, 2, 3], [4, 5, 6]], dtype=complex)
```
所创建的数组长什么样子？
?
```
array([[1.+0.j, 2.+0.j, 3.+0.j],[4.+0.j, 5.+0.j, 6.+0.j]])
```

31.A是一个numpy数组`print(A[A < 0.5])`输出结果是什么？
?
具体来说，A < 0.5 会生成一个布尔数组，其中每个元素对应于A中相同位置的元素是否小于0.5。然后，`A[A < 0.5]`使用这个布尔数组作为索引，返回A中所有小于0.5的元素。

32.`df.isin([50, 40])` 做了什么？
?
会检查 DataFrame df 中的每个元素是否为 50 或 40，并返回一个布尔值 DataFrame。

33.检查 (DataFrame)Grade 列中的每个元素是否为 'E'
?
`df['Grade'].isin(['E'])`

34.检查DataFrame多列中的每个元素是否是预想值用什么？比如检查age和Grade
?
```
# 同时检查 age=50/30 AND Grade='A'/'B'
multi_check = df.isin({
    'age': [50, 30],
    'Grade': ['A', 'B']
})
```

35.遍历数组中的每一个元素
?
for item in A.flat:

36A.flat与A.flatten() 的区别
?
![[Pasted image 20250425120748.png]]

37.
```
s = pd.Series([12, -4, 7, 9], index=['a', 'b', 'c', 'd'])
```
怎么获取s的索引和值
?
```
s.index
>>> Index(['a', 'b', 'c', 'd'], dtype='object')
s.values
>>>array([12, -4,  7,  9])
```

38.根据numpy数组创建的Series,当数组中的元素值发生改变时，Series中的值会不会被影响？
?
会，因为底层数据是直接引用原始 NumPy 数组的内存地址（而非复制数据）。

39.np.log()、np.sqrt()、np.sin()、np.cos()分别的作用是
?
传入数组，就会对数组中的每一个元素都进行对数值、平方根、sin值、cos值的计算

40.获取Series中的唯一值数组用什么方法
?
```
s = pd.Series(['c', 'a', 'd', 'a', 'a', 'b', 'b', 'c', 'c'])
uniques = s.unique()
print(uniques)  # 输出: array(['c', 'a', 'd', 'b'], dtype=object)
uniques.sort()
print(uniques)  # 输出: array(['a', 'b', 'c', 'd'], dtype=object)
```

41.算一个 Series 中各值出现的频率?
?
```
s = pd.Series(['c', 'a', 'd', 'a', 'a', 'b', 'b', 'c', 'c'])
print(s.value_counts())
# 输出:
# a    3
# c    3
# b    2
# d    1
# dtype: int64
```

42.
```
   s1 = pd.Series([10, 20, 30], index=['a', 'b', 'c'])
   s2 = pd.Series([40, 50], index=['b', 'd'])
   result = s1 + s2
   print(result)
```
结果是？
?
```
   a    NaN
   b    70.0
   c    NaN
   d    NaN
   dtype: float64
```

43.怎么避免Series相加时因为标签不对应而导致输出NaN值？
```
   s1 = pd.Series([10, 20, 30], index=['a', 'b', 'c'])
   s2 = pd.Series([40, 50], index=['b', 'd'])
   result = s1 + s2
   print(result)
```
?
```
   result = s1.add(s2, fill_value=0)
   print(result)
   #输出结果是：
   a    10.0
   b    70.0
   c    30.0
   d     0.0
   dtype: float64
```


44.
```
data = {
         'color': ['blue', 'green', 'yellow', 'red', 'white'],
         'object': ['ball', 'pen', 'pencil', 'paper', 'mug'],
         'price': [1.2, 1.0, 0.6, 0.9, 1.7]
     }
```
`df= pd.DataFrame(data, columns=['object', 'price'])`起到的作用？如果指定的列在字典中不存在那么？
?
输出：
```
       object  price
     0   ball    1.2
     1    pen    1.0
     2 pencil    0.6
     3  paper    0.9
     4    mug    1.7
```
不存在那么会用NaN填充这些列

45.用什么方法遍历 Series 中的所有元素，找到其中最小值，并返回该最小值对应的索引？找到其中最大值，并返回该最大值对应的索引？
?
```
import pandas as pd

# 创建一个 Series，存储学生姓名及其考试成绩
scores = pd.Series(
    [85, 92, 78, 88, 95],
    index=["Alice", "Bob", "Charlie", "David", "Eve"]
)
lowest_score_student = scores.idxmin()
print("最低分的学生:", lowest_score_student)
highest_score_student = scores.idxmax()
print("最高分的学生:", highest_score_student)
#输出：
最低分的学生: Charlie
最高分的学生: Eve
```

46.检查Series或者DataFrame中数据是否全部为唯一值？
?
```
import numpy as np
s = pd.Series([1, np.nan, np.nan])
print(s.is_unique)   # Output: False（因为NaN重复）
# 忽略NaN后检查
print(s.dropna().is_unique)   # Output: True


df = pd.DataFrame({'A': [1, 2, 3], 'B': ['x', 'x', 'y']})
print(df['A'].is_unique)   # Output: True（A列唯一）
print(df['B'].is_unique)   # Output: False（B列重复）
```

47.
```
ser = pd.Series([2, 5, 7, 4], index=['one', 'two', 'three', 'four'])
>>> ser.reindex(['three', 'four', 'five', 'one'])
```
输出结果会是什么？为什么是这样的
?
```
one    2
two    5
three  7
four   4
dtype: int64
```
![[Pasted image 20250425132619.png]]

48.
```
ser3 = pd.Series([1, 5, 6, 3], index=[0, 3, 5, 6])
>>> ser3.reindex(range(7), method='ffill')#或者ser3.reindex(range(7), method='bfill')呢？
```
输出结果是什么？
?
```
原始结果：
   0    1
   3    5
   5    6
   6    3
   dtype: int64
重新索引并向前填充：
0    1
1    1
2    1
3    5
4    5
5    6
6    3
dtype: int64
```
range(7)这表示希望 Series 的索引从 0 到 6 连续，bfill是向后填充

49.删除 Series 中指定的标签？会影响原来的吗？比如
```
   import pandas as pd
   import numpy as np

   ser = pd.Series(np.arange(4.), index=['red', 'blue', 'yellow', 'white'])
```
我想删除'yellow'
?
```
new_ser = ser.drop('yellow')
#输出：
   red    0.0
   blue   1.0
   white  3.0
   dtype: float64
```
不会影响原来的

50.根据标签删除 DataFrame 中指定行或列？
?
```
   df = pd.DataFrame(np.arange(12).reshape(3, 4), columns=['A', 'B', 'C', 'D'])
   # 删除列
   new_df = df.drop(['B', 'C'], axis=1)
   print(new_df)

   # 删除行
   new_df = df.drop([0, 1])
   print(new_df)
   #输出：
      A  D
   0  0  3
   1  4  7
   2  8  11

      A  B  C   D
   2  8  9  10  11
```

51.使用什么参数可以用drop之后直接修改原数据？
?
```
   df.drop(['B', 'C'], axis=1, inplace=True)#直接在原数据上删除列
```

52.