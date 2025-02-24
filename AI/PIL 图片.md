**PIL（Python Imaging Library）图片**指的是由**PIL**库或其继承版本**Pillow**处理的图像数据。

### **PIL 和 Pillow 的关系**

- **PIL（Python Imaging Library）** 是 Python 早期的一个图像处理库，提供了强大的功能来打开、编辑、转换和保存多种格式的图片。
- **Pillow** 是 **PIL 的一个分支（Fork）**，在 PIL 停止维护后，Pillow 继承了 PIL 的所有功能，并增加了许多新特性，兼容 Python 3，因此现在一般都使用 **Pillow** 而不是 PIL。

### **PIL（Pillow）能处理哪些图片格式？**

Pillow 支持多种常见的图片格式，如：

- **JPEG**（.jpg）
- **PNG**（.png）
- **BMP**（.bmp）
- **GIF**（.gif）
- **TIFF**（.tiff）
- 以及其他更少见的格式。

### **PIL 图片的基本操作**

1. **安装 Pillow**
    
    ```bash
    pip install pillow
    ```
    
2. **加载一张图片**
    
    ```python
    from PIL import Image
    
    img = Image.open("example.jpg")  # 打开一张图片
    img.show()  # 显示图片
    ```
    
3. **获取图片信息**
    
    ```python
    print(img.format)  # 输出格式（如 JPEG、PNG）
    print(img.size)    # 输出尺寸 (宽, 高)
    print(img.mode)    # 输出模式（如 RGB, L, CMYK）
    ```
    
4. **转换图片模式（如灰度图）**
    
    ```python
    gray_img = img.convert("L")  # 转换为灰度图
    gray_img.show()
    ```
    
5. **调整图片尺寸**
    
    ```python
    resized_img = img.resize((200, 200))  # 调整到 200x200
    resized_img.show()
    ```
    
6. **裁剪图片**
    
    ```python
    cropped_img = img.crop((50, 50, 200, 200))  # 裁剪区域 (左, 上, 右, 下)
    cropped_img.show()
    ```
    
7. **保存图片**
    
    ```python
    img.save("new_image.png")  # 以 PNG 格式保存
    ```
    

### **PIL 图片在 PyTorch 里的应用**

在 PyTorch 训练深度学习模型时，我们通常会使用 `PIL` 读取图片并转换成 PyTorch 的 `Tensor` 格式：

```python
from PIL import Image
import torchvision.transforms as transforms

img = Image.open("example.jpg")  # 读取图片
transform = transforms.ToTensor()  # 转换为 Tensor
tensor_img = transform(img)
print(tensor_img.shape)  # 输出 (C, H, W)，即 (通道, 高度, 宽度)
```

### **总结**

- **PIL（Pillow）** 是 Python 处理图片的核心库，能够打开、编辑、转换和保存多种格式的图片。
- 现代 Python 版本通常使用 **Pillow**，因为它是对 PIL 的改进版本。
- **Pillow 可以与 PyTorch、OpenCV 等库结合使用**，广泛应用于深度学习和计算机视觉任务中。

如果你要处理图片数据，学习 PIL（Pillow） 是非常必要的！ 😊