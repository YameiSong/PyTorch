# 通过二进制文件安装

## Anaconda

如果你想通过 Anaconda 安装 PyTorch，请点击“开始 &gt; Anaconda3 &gt; Anaconda Prompt”来打开 Anaconda Prompt。

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