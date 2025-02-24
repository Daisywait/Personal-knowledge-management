**NumPy 数组（NumPy Array）** 是 **NumPy（Numerical Python）** 库提供的一种用于存储和处理多维数据的核心数据结构，通常叫 **ndarray（N-dimensional array）**。它类似于 Python 的列表（list），但更高效、功能更强大，适用于大规模数据运算，如矩阵运算、统计分析、机器学习等。

---

## **1. NumPy 数组 vs Python 列表**

Python 自带的 **list** 也可以存储数字，但 NumPy 数组相比 Python 列表有以下优势：

- **占用更少的内存**：NumPy 数组的存储方式更紧凑，避免了 Python 列表的额外开销。
- **运算速度更快**：NumPy 采用 C 语言实现，底层进行优化，运算速度比 Python 原生 list 快 **几十倍甚至上百倍**。
- **支持向量化运算**：NumPy 数组可以进行批量计算，而不需要使用 `for` 循环，提高计算效率。
- **支持多维数组**：NumPy 直接支持 **多维数组（矩阵）**，而 Python 的 list 需要嵌套列表才能实现。

---

## **2. NumPy 数组的基本操作**

### **（1）安装 NumPy**

如果还没有安装 NumPy，可以用 `pip` 进行安装：

```bash
pip install numpy
```

### **（2）创建 NumPy 数组**

```python
import numpy as np  # 导入 NumPy 并简写为 np

# 创建一维数组
arr1 = np.array([1, 2, 3, 4, 5])
print(arr1)  # 输出: [1 2 3 4 5]
print(type(arr1))  # <class 'numpy.ndarray'>

# 创建二维数组（矩阵）
arr2 = np.array([[1, 2, 3], [4, 5, 6]])
print(arr2)
# 输出：
# [[1 2 3]
#  [4 5 6]]

# 创建全 0 数组
zeros_arr = np.zeros((2, 3))  # 2行3列的全零矩阵
print(zeros_arr)

# 创建全 1 数组
ones_arr = np.ones((3, 3))  # 3x3 全 1 矩阵
print(ones_arr)

# 创建随机数组
rand_arr = np.random.rand(3, 3)  # 3x3 0~1 之间的随机数
print(rand_arr)
```

---

### **（3）NumPy 数组的属性**

```python
arr = np.array([[1, 2, 3], [4, 5, 6]])

print(arr.shape)  # 形状 (2, 3)，表示 2 行 3 列
print(arr.ndim)   # 维度 2
print(arr.size)   # 总元素个数 6
print(arr.dtype)  # 数据类型，例如 int32 或 float64
```

---

### **（4）数组的索引和切片**

NumPy 数组的索引规则与 Python 列表类似，但功能更强大：

```python
arr = np.array([[10, 20, 30], [40, 50, 60]])

# 访问单个元素
print(arr[0, 1])  # 访问第 1 行，第 2 列（索引从 0 开始），输出 20

# 切片（获取部分数组）
print(arr[:, 1])  # 取所有行的第 2 列，输出 [20 50]
print(arr[1, :])  # 取第 2 行的所有列，输出 [40 50 60]
```

---

### **（5）数组的运算**

NumPy 支持**向量化运算**，可以直接进行数学运算，而不需要 `for` 循环：

```python
arr = np.array([1, 2, 3, 4])

print(arr + 10)  # 加法，每个元素 +10
# 输出: [11 12 13 14]

print(arr * 2)  # 乘法，每个元素 *2
# 输出: [ 2  4  6  8]

print(arr ** 2)  # 平方
# 输出: [ 1  4  9 16]

# 两个数组相加
arr2 = np.array([5, 6, 7, 8])
print(arr + arr2)  # [ 6  8 10 12]
```

---

### **（6）矩阵运算**

NumPy 非常适合处理矩阵计算，例如：

```python
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

# 矩阵相加
print(A + B)
# [[ 6  8]
#  [10 12]]

# 矩阵乘法（逐元素相乘）
print(A * B)
# [[ 5 12]
#  [21 32]]

# 矩阵点乘（矩阵乘法）
print(A @ B)  # 或者 np.dot(A, B)
# [[19 22]
#  [43 50]]
```

---

## **3. NumPy 在 PyTorch 和机器学习中的应用**

在 PyTorch 或机器学习中，**数据通常以 NumPy 数组的形式存储和处理**，然后转换为 PyTorch 张量（Tensor）：

```python
import torch
import numpy as np

# NumPy 转 PyTorch Tensor
np_array = np.array([[1, 2], [3, 4]])
torch_tensor = torch.from_numpy(np_array)
print(torch_tensor)
# 输出：
# tensor([[1, 2],
#         [3, 4]], dtype=torch.int32)

# PyTorch Tensor 转 NumPy
numpy_array = torch_tensor.numpy()
print(numpy_array)
```

---

## **4. 什么时候用 NumPy？**

- **数据处理**：读取、存储、操作大规模数据，如 CSV、Excel 文件。
- **数学运算**：向量、矩阵计算、统计分析（如均值、标准差等）。
- **机器学习**：NumPy 是 Scikit-Learn、TensorFlow、PyTorch 等深度学习库的基础。
- **科学计算**：用 NumPy 进行数据分析、数值计算和图像处理。

---

## **5. 总结**

- **NumPy 是 Python 进行数值计算的核心库**，比 Python 自带的 `list` **更快、更高效**。
- **NumPy 数组（ndarray）可以是多维的**，支持高效的数学运算。
- **NumPy 支持向量化计算**，不需要 `for` 循环，计算速度远超 Python 列表。
- **NumPy 在机器学习和深度学习中至关重要**，数据通常以 NumPy 数组存储。

如果你想学 PyTorch、机器学习，先学会 **NumPy** 是非常重要的！ 🚀