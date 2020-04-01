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
