# 前期准备

## 支持的 Windows 版本

以下 Windows 发行版本支持 PyTorch：

* __最低:__ Windows 7, Windows Server 2008 r2
* __推荐:__ Windows 10+, Windows Server 2019+

## Python

目前，Windows 上的 PyTorch 仅支持 Python 3.x 版本，不再支持 Python 2.x 版本。

Windows 系统默认未安装 Python，你可以通过以下方法安装 Python：

### Anaconda

通过 Anaconda 安装 PyTorch 的过程中，Anaconda 将自动安装 Python 的沙盒版本来运行 PyTorch 程序，因此无需额外安装 Python。

### Python官网

你可以访问[Python 官方网站](https://www.python.org/downloads/windows/)，下载并安装最新的 Python 3 版本。

### Chocolatey

[Chocolatey](https://chocolatey.org/)是 Windows 的程序包管理器。 如果你已安装 Chocolatey，请按照以下步骤安装 Python：

1. 右键单击“开始”按钮，然后点击“Windows PowerShell（管理员）”，以通过管理员身份运行 PowerShell。
2. 在 PowerShell 中，运行如下命令：

```
choco install python
```

**注意：** 在 PowerShell 中运行指令 `py -V` 可查看 Python 版本。

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

请按以下步骤升级 GPU 的驱动程序：

1. 右键单击 Windows 系统桌面空白处，点击“NVIDIA 控制面板”。
2. 打开“帮助”菜单，然后点击“更新”。
3. 在“更新”标签页中，点击“检查更新”。
4. 按照 NVIDIA 的说明将 GPU 驱动程序升级到最新版本。