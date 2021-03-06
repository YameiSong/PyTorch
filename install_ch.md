# 目录

* [前期准备](install_ch.md#前期准备)
* [通过二进制文件安装](install_ch.md#通过二进制文件安装)
* [通过源代码安装](install_ch.md#通过源代码安装)
* [验证](install_ch.md#验证)

# 前期准备

## 支持的 Windows 版本

以下 Windows 发行版本支持 PyTorch：

* 最低: Windows 7, Windows Server 2008 r2
* 推荐: Windows 10+, Windows Server 2019+

## Python

目前，Windows 上的 PyTorch 仅支持 Python 3.x 版本，不再支持 Python 2.x 版本。

Windows 系统默认未安装 Python，你可以通过以下三种方法安装 Python。

### Anaconda

通过 Anaconda 安装 PyTorch 的过程中，Anaconda 将自动安装 Python 的沙盒版本来运行 PyTorch 程序，因此无需额外安装 Python。

### Python官网

你可以访问 [Python 官方网站](https://www.python.org/downloads/windows/)，下载并安装最新的 Python 3 版本。

### Chocolatey

[Chocolatey](https://chocolatey.org/) 是 Windows 的程序包管理器。 如果你已安装 Chocolatey，请按照以下步骤安装 Python：

1. 右键单击“开始”按钮，然后点击“Windows PowerShell（管理员）”，以通过管理员身份运行 PowerShell。
2. 在 PowerShell 中，运行如下命令：

```
choco install python
```

**注意：** 在 PowerShell 中运行指令 `py -V` 或 `python -V` 可查看 Python 版本。

## 程序包管理器

若以二进制文件方式安装 PyTorch，你至少需要安装以下两个程序包管理器中的一个：[Anaconda](https://www.anaconda.com/distribution/#windows) 和 [pip](https://pypi.org/project/pip/)。推荐使用 Anaconda 程序包管理器，因为它将在沙盒环境中为你安装全部的 PyTorch 依赖项，包括 Python 和 pip。

### Anaconda

请按以下步骤安装 Anaconda: 

1. 通过 [Anaconda](https://www.anaconda.com/distribution/#windows) 网站, 下载“64-bit graphical installer”安装程序。
2. 运行安装程序，并应用所有默认选项来安装 Anaconda。

### pip

如果你使用以上推荐的任意一种方式安装了 Python，那么你已经完成了 [pip](https://pypi.org/project/pip/) 的安装。

**注意：** 在 PowerShell 中运行指令 `pip -V` 可查看 pip 版本。

## CUDA

为了充分利用 PyTorch 的 [CUDA](https://pytorch.org/tutorials/beginner/blitz/tensor_tutorial.html?highlight=cuda#cuda-tensors) 功能，建议使用配备 NVIDIA GPU 的 Windows 系统。

请按以下步骤验证你的 GPU 是否支持 CUDA：

1. 右键单击“开始”按钮，选择“设备管理器”。
2. 展开“显示适配器”，然后查看显卡的供应商名称和型号。
3. 如果你的 NVIDIA 显卡型号位于 [CUDA GPUs](http://developer.nvidia.com/cuda-gpus) 列表中，则该显卡支持 CUDA。

![](assets/gpu_ch.png)

请按以下步骤升级 GPU 的驱动程序：

1. 右键单击 Windows 系统桌面空白处，点击“NVIDIA 控制面板”。
2. 打开“帮助”菜单，然后点击“更新”。
3. 在“更新”标签页中，点击“检查更新”。
4. 按照 NVIDIA 的说明将 GPU 驱动程序升级到最新版本。

请按以下步骤查看你的 CUDA 版本：

1. 在“NVIDIA 控制面板”中，点击左下角的“系统信息”。
2. 在“组件 &gt; 3D 设置”区域，通过“NVCUDA.DLL”文件的产品名称查看 CUDA 版本。

![](assets/cuda_ch.png)

# 通过二进制文件安装

## Anaconda

如果你想通过 Anaconda 安装 PyTorch，请点击“开始 &gt; Anaconda3 &gt; Anaconda Prompt”来运行 Anaconda Prompt。

### 不含 CUDA 功能

如果你想通过 Anaconda 安装 PyTorch，并且你的机器不支持 [CUDA](https://developer.nvidia.com/cuda-zone) 功能或者你不需要使用 CUDA 功能，请运行下面的指令：

```
conda install pytorch torchvision cpuonly -c pytorch
```

### 包含 CUDA 功能

如果你想通过 Anaconda 安装 PyTorch，并且你的机器支持 [CUDA](https://developer.nvidia.com/cuda-zone) 功能，请根据机器的 CUDA 版本在下方选择一个指令并运行：

#### CUDA 9.2

```
conda install pytorch torchvision cudatoolkit=9.2 -c pytorch -c defaults -c numba/label/dev
```

#### CUDA 10.1

```
conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
```
## pip

如果你想通过 pip 安装 PyTorch，请右键单击“开始”按钮，然后点击“Windows PowerShell”来运行 PowerShell。

### No CUDA

如果你想通过 pip 安装 PyTorch，并且你的机器不支持 [CUDA](https://developer.nvidia.com/cuda-zone) 功能或者你不需要使用 CUDA 功能，请运行下面的指令：

```
pip install torch==1.4.0+cpu torchvision==0.5.0+cpu -f https://download.pytorch.org/whl/torch_stable.html
```

### With CUDA

如果你想通过 pip 安装 PyTorch，并且你的机器支持 [CUDA](https://developer.nvidia.com/cuda-zone) 功能，请根据机器的 CUDA 版本在下方选择一个指令并运行：

#### CUDA 9.2

```
pip install torch==1.4.0+cu92 torchvision==0.5.0+cu92 -f https://download.pytorch.org/whl/torch_stable.html
```

#### CUDA 10.1

```
pip install torch===1.4.0 torchvision===0.5.0 -f https://download.pytorch.org/whl/torch_stable.html
```

# 通过源代码安装

对于大多数 PyTorch 用户来说，通过程序包管理器安装预先构建的二进制文件是最佳的选择。但是，有时出于测试或者开发需求，你可能需要安装最新的 PyTorch 代码。对于这种情况，你可以从源代码构建 PyTorch。

## 前期准备

1. 安装 [Anaconda](install_ch.md#anaconda-1)。
2. 如果你的机器安装了[支持 CUDA 功能的 GPU]((https://developer.nvidia.com/cuda-gpus))，请下载并安装 [CUDA](https://developer.nvidia.com/cuda-downloads)。
3. 若要在 Windows 上构建 PyTorch，你还需要安装 Visual Studio 2017 14.11 工具集和 NVTX。尤其对于构建在 Windows 上的 CUDA 8 而言，你需要额外安装 VS 2015 Update 3 和一个补丁。你可以在[这里](https://support.microsoft.com/en-gb/help/4020481/fix-link-exe-crashes-with-a-fatal-lnk1000-error-when-you-use-wholearch)查看补丁的详细信息。
4. 按照[这里](https://github.com/pytorch/pytorch#from-source)描述的步骤，从源代码构建 PyTorch。

# 验证

你可以通过运行 PyTorch 的示例代码来验证是否正确安装了 PyTorch。接下来你将构造一个随机初始化的 tensor。

首先，点击“开始 &gt; Anaconda3 &gt; Anaconda Prompt”来打开 Anaconda Prompt，并运行 `python` 指令。

然后，输入以下代码：

```python
from __future__ import print_function
import torch
x = torch.rand(5, 3)
print(x)
```

运行结果应该类似于：

```python
tensor([[0.1935, 0.5487, 0.1230],
        [0.5119, 0.6789, 0.6307],
        [0.8938, 0.3003, 0.3712],
        [0.6285, 0.1104, 0.8474],
        [0.7535, 0.3999, 0.3722]])
```

另外，运行以下命令来检查你的 GPU 驱动和 CUDA 功能是否被 PyTorch 启用和访问：

```python
torch.cuda.is_available()
```