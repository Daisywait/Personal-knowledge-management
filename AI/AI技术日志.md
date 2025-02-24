# 技术日志

● 1月

● 1、机器学习体验

● Google Teachable Machine训练，文件夹下：cup+notcup，导出模型之后嵌入网页中需要用tensorflow.js框架和前端：三个文件html+css+json，在vscode可以实时看效果

![](file:///C:\Users\HP\AppData\Local\Temp\ksohtml24028\wps4.jpg) 

● 问题是为什么模型的准确度不高?

● 2、wsl命令行

● (1)在VScode终端输入ctrl+`打开终端，然后安装Windows Subsystem for Linux，用wsl --install安装，之后默认安装的是wsl2，还需要安装linux发行版Ubuntu，用命令wsl --install -d Ubuntu，安装完之后在vscode终端输入wsl，接着就可以用下面的命令查找：find /mnt/c/Users/HP/ -name "*.png" > results.txt

![](file:///C:\Users\HP\AppData\Local\Temp\ksohtml24028\wps5.jpg) 

● 问题是都用sudo了，为什么有一些文件还是permission denied

● (2)用awk统计CSV文件某列的平均值  

● awk -F',' 'NR>1 {sum+=$3; count++} END {print "平均数量:", sum/count}' data.csv

![](file:///C:\Users\HP\AppData\Local\Temp\ksohtml24028\wps6.jpg) 

● 用python文件生成csv测试数据：在上powershell的终端上输入python 生成csv.py（格式是python空格文件名）

● (3)写bash脚本批量重命名100个txt文件

● 写了两个脚本，一个是generate一个是重命名文件

● 问题是脚本语法还不知道，但是知道开头是#!/bin/bash

● 3、多平台输出hello,world.py

● (1)github提交代码文件：在本地cmd先创建目录文件，之后git init 初始化仓库，接着echo.> hello.py新建文件，notepad打开并且编辑代码，然后git add . 暂存到本地仓库中，之后进行git commit -m"test_hello",之后关联远程仓库：git remote add origin [https://github.com/Daisywait/test](https://github.com/Daisywait/test)，地址是仓库的URL。接着查看当前分支git branch，输出*master,表示当前本地分支是master,后面就可以直接推送了git push -u origin master->推送 master 并设置 origin/master 为上游，以后可直接 git push(-u表示设置上游为origin/master)

● (2)用kaggle提交了代码，挺简单的，就是点击左侧的运行键就可以了

● (3)云服务器

暂时要付钱

● (4)Arduino开发板  

没有硬件设备Arduino开发板 ​

● (5)微信小程序开发者工具：[https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)遇到了下面的问题，是一新建项目之后就遇到了这个东西

[渲染层错误] Uncaught ReferenceError: Trace is not defined(env: Windows,mp,1.06.2412050; lib: 2.25.3) [渲染层错误] ReferenceError: SystemError (webviewScriptError) Trace is not defined(env: Windows,mp,1.06.2412050; lib: 2.25.3)

● 2月

●  项目 1：用 Python 训练一个手写数字识别模型（VScode[powershell]+python解释器+库）

● 命令解释：

● where python（确认已经下载python）

	●C:\msys64\mingw64\bin\python.exe

	这是 **MSYS2** 安装的 Python 解释器，用于 MSYS2 环境。它与 Anaconda 没有关系。

	● C:\Users\HP\AppData\Local\Programs\Python\Python313\python.exe

	这是你 **手动安装的 Python 3.13** 的解释器。它也与 Anaconda 没有关系。

	● C:\Users\HP\AppData\Local\Microsoft\WindowsApps\python.exe

	这是 Windows 自带的 **占位符** python.exe，并不是一个实际的 Python 解释器。它用于引导你到 Microsoft Store 安装 Python。

● python -m ensurepip --default-[[pip]]

	python -m ensurepip 是一个 Python 模块，它会确保在当前的 Python 环境中安装 pip（Python 的包管理工具）。 --default-pip 参数会安装或更新 pip 到当前 Python 解释器所使用的版本。

● pip install torch torchvision matplotlib

	在 **PowerShell** 中执行 pip install torch torchvision matplotlib 这个命令时，它会默认安装到你当前激活的 **Python 环境** 中。上面是 pip install torch torchvision matplotlib 这条命令是用来安装三个非常常见的 Python 库，它们分别用于不同的任务，特别是在深度学习和计算机视觉领域。

● 终端输出解释

● VScode终端输入py python文件名，后输出：Epoch 1, Loss: 0.15322646498680115；Epoch 2, Loss: 0.1603385955095291；Epoch 3, Loss: 0.12767164409160614

	**Epoch（训练轮次）**        
	Epoch 1: 代表第一轮训练完成后        
	Epoch 2: 代表第二轮训练完成后        
	Epoch 3: 代表第三轮训练完成后 
	
	Loss（损失值）** **损失值（Loss）** 是用来衡量模型预测结果与真实标签的误差的指标，通常越小越好。        
	Loss: 0.15322646498680115        
	Loss: 0.1603385955095291        
	Loss: 0.12767164409160614 
	**如何理解这个输出？** **Epoch 1 → Loss: 0.1532** **Epoch 2 → Loss: 0.1603（比上一轮稍微大了一点）** **Epoch 3 → Loss: 0.1276（下降了，说明模型在学习）** 通常，训练过程中 **Loss 逐渐降低**，说明模型在逐步优化。 但如果 **Loss 反复增减**，可能是： **学习率过大**：模型在不同方向上跳跃，收敛不稳定。 **数据噪声大**：数据本身有随机性，导致损失值波动。 **过拟合或欠拟合**：模型可能学得太好或太差。

● 代码解释：该代码使用了PyTorch训练一个简单神经网络来识别手写数字，用到的[[python语法规则]]

● 导入部分：import 语句是**Python 导入库（modules）的操作，主要用于 PyTorch 深度学习 相关任务。

● import [[torch]]

●  import [[torchvision]]

●  import torchvision.transforms as [[transforms]]

●  import [[torch.nn]] as nn

● import [[torch.optim]] as optim import matplotlib.pyplot as plt


● 1. 定义转换规则和加载 MNIST 数据集

● transform = transforms.Compose([transforms.ToTensor(), transforms.Normalize((0.5,), (0.5,))])

 - transforms.Compose([...]) **作用**：把多个转换操作组合在一起，形成一个完整的**预处理管道**。  transforms.ToTensor()**作用**： 把 **[[PIL 图片]]** 或 **[[NumPy 数组]]** 转换成 **PyTorch 的 Tensor（张量）**。 同时，会把[[图片像素值]] *从 (0 ~ 255) [[归一化]]到 (0 ~ 1)**。

● trainset = torchvision.datasets.MNIST([[root]]='./data', [[train=True]], [[download=True]], transform=transform)加载数据集，[[MNIST 数据集]]中的图片**原始格式是 PIL 图片**（Python Imaging Library）。当 `transform` 里使用 `ToTensor()` 之后，PIL 图片就会转换成 PyTorch 的 `Tensor`，变成数值化的数据，方便进行**归一化、输入神经网络**等操作。 **`transform=transform`
***应用 `transform` 预处理**：
    - `transform=transform` 让加载的图片**自动转换为 Tensor，并进行归一化**。

● trainloader = [[torch.utils.data.DataLoader]](trainset, batch_size=64, shuffle=True)

●2.可视化一个图片
●images, labels = next(iter(trainloader))


● 补充

● npm 是 **Node.js 的包管理工具**

全称是：**Node Package Manager**（Node.js 包管理器）它的作用类似于 pip 之于 Python，主要用于 **安装、管理 JavaScript 相关的库**，特别是在 **前端开发** 和 **Node.js 服务器开发** 中常用。

● Anaconda[https://www.anaconda.com/](https://www.anaconda.com/)下载发行版，安装好了后在Anaconda Prompt输入conda info：里面会出现 base environment : D:\anaconda3  (writable)之类的地址和信息

Anaconda 是一个专门用于数据科学和机器学习的 Python 发行版，它集成了 Python 解释器、大量常用的科学计算库（如 NumPy、Pandas、Matplotlib、Scikit-Learn、TensorFlow 等）以及一个包管理工具 conda。 **Anaconda 的核心特点** **内置常用库**：安装后自带多个数据科学相关的库，无需单独安装，省去环境配置的麻烦。 **conda 环境管理**：支持创建、管理、切换不同的 Python 版本和库环境，解决库版本冲突问题。 **兼容 Jupyter Notebook**：自带 Jupyter Notebook 方便进行交互式编程和数据分析。 **跨平台支持**：支持 Windows、Mac 和 Linux。 **Anaconda vs. 普通 Python** 特性Anaconda纯 Python (如官方的 CPython) 主要用途    数据科学、机器学习、科学计算    通用编程、Web 开发等 包管理工具    conda（也支持 pip）    主要用 pip 默认安装体积    较大，约 1~2 GB    轻量，几十 MB 内置库    自带大量数据科学库    需要手动安装 **是否需要安装 Anaconda？** 如果你的主要目标是 **数据科学、机器学习**，Anaconda 是一个方便的选择，环境管理和库安装都更简单。 如果你想要 **更灵活、更轻量** 的环境（比如 Web 开发），可以直接使用普通 Python 并搭配 pip。