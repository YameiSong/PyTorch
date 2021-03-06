# Table of Contents

* [Prerequisites](install_en.md#prerequisites)
* [Building From Binaries](install_en.md#building-from-binaries)
* [Building From Source](install_en.md#building-from-source)
* [Verification](install_en.md#verification)

# Prerequisites

## Supported Windows Distributions

PyTorch is supported on the following Windows distributions:

* __Minimum:__ Windows 7, Windows Server 2008 r2
* __Recommended:__ Windows 10+, Windows Server 2019+

## Python

Currently, PyTorch on Windows only supports Python 3.x; Python 2.x is not supported.

As it is not installed by default on Windows, there are multiple ways to install Python:

### Anaconda

If you use Anaconda to install PyTorch, it will install a sandboxed version of Python that will be used for running PyTorch applications. In other words, you don't need to install Python yourself.

### Python Website

You can go to the [Python website](https://www.python.org/downloads/windows/) to download and install the latest Python 3 release.

### Chocolatey

[Chocolatey](https://chocolatey.org/) is a package manager for Windows. If you have installed Chocolatey, follow the steps below to install Python:

1. Right-click the **Start** button, and then click **Windows PowerShell (Admin)** to run your PowerShell as an administer.
2. In the PowerShell, run the command below:

```
choco install python
```

_**NOTE:**_ To check Python version, run `py -V` or `python -V` in PowerShell.

## Package Manager

To install the PyTorch binaries, you will need to use at least one of two supported package managers: [Anaconda](https://www.anaconda.com/distribution/#windows) and [pip](https://pypi.org/project/pip/). Anaconda is the recommended package manager as it will provide you all of the PyTorch dependencies in one, sandboxed installation, including Python and pip.

### Anaconda

To install Anaconda: 

1. On the [Anaconda](https://www.anaconda.com/distribution/#windows) website, download the 64-bit graphical installer.
2. Run the installer, and then apply all default options to install Anaconda.

### pip

If you installed Python by any of the recommended ways above, [pip](https://pypi.org/project/pip/) will have already been installed for you.

_**NOTE:**_ To check pip version, run `pip -V` in PowerShell.

## CUDA

It is recommended, but not required, that your Windows system has an NVIDIA GPU in order to harness the full power of PyTorch’s [CUDA support](https://pytorch.org/tutorials/beginner/blitz/tensor_tutorial.html?highlight=cuda#cuda-tensors).

To verify you have a CUDA-Capable GPU:

1. Right-click the **Start** button, and then click **Device Manager.** 
2. Expand the **Display Adapters** section, then you will find the vendor name and model of your graphics card(s).
3. If you have an NVIDIA card that is listed in [CUDA GPUs](http://developer.nvidia.com/cuda-gpus), that GPU is CUDA-capable.

![](assets/gpu_en.png)

To upgrade GPU driver:

1. Right-click on the Windows desktop and click **NVIDIA Control Panel.**
2. Navigate to the **Help** menu and click **Updates.**
3. In the **Updates** tab, click **Check for Updates.**
4. Follow the instructions from NVIDIA to upgrade your GPU driver to the latest version.

To check your CUDA version:

1. In the **NVIDIA Control Panel**, click **System Information** at the bottom left corner. 
2. Navigate to **Components &gt; 3D Settings**, and then check your CUDA version in the **Product Name** of **NVCUDA.DLL** file.

![](assets/cuda_en.png)

# Building From Binaries

## Anaconda

To install PyTorch with Anaconda, you will need to open an Anaconda prompt via **Start &gt; Anaconda3 &gt; Anaconda Prompt.**

### No CUDA

To install PyTorch via Anaconda, and do not have a [CUDA-capable](https://developer.nvidia.com/cuda-zone) system or do not require CUDA, run the following command:

```
conda install pytorch torchvision cpuonly -c pytorch
```

### With CUDA

To install PyTorch via Anaconda, and you do have a [CUDA-capable](https://developer.nvidia.com/cuda-zone) system, run one of the following commands based on the CUDA version suited to your machine:

#### CUDA 9.2

```
conda install pytorch torchvision cudatoolkit=9.2 -c pytorch -c defaults -c numba/label/dev
```

#### CUDA 10.1

```
conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
```

## pip

To install PyTorch with pip, please right-click the **Start** button, and then click **Windows PowerShell** to run your PowerShell.

### No CUDA

To install PyTorch via pip, and do not have a CUDA-capable system or do not require CUDA, run the following command:

```
pip install torch==1.4.0+cpu torchvision==0.5.0+cpu -f https://download.pytorch.org/whl/torch_stable.html
```

### With CUDA

To install PyTorch via pip, and do have a CUDA-capable system, run one of the following commands based on the CUDA version suited to your machine:

#### CUDA 9.2

```
pip install torch==1.4.0+cu92 torchvision==0.5.0+cu92 -f https://download.pytorch.org/whl/torch_stable.html
```

#### CUDA 10.1

```
pip install torch===1.4.0 torchvision===0.5.0 -f https://download.pytorch.org/whl/torch_stable.html
```

# Building From Source

For the majority of PyTorch users, installing from a pre-built binary via a package manager will provide the best experience. However, there are times when you may want to install the bleeding edge PyTorch code, whether for testing or actual development on the PyTorch core. To install the latest PyTorch code, you will need to build PyTorch from source.

## Prerequisites

1. Install [Anaconda](install_en.md#anaconda-1).
2. Install [CUDA](https://developer.nvidia.com/cuda-downloads), if your machine has a [CUDA-enabled GPU](https://developer.nvidia.com/cuda-gpus).
3. If you want to build on Windows, Visual Studio 2017 14.11 toolset and NVTX are also needed. Especially, for CUDA 8 build on Windows, there will be an additional requirement for VS 2015 Update 3 and a patch for it. The details of the patch can be found out [here](https://support.microsoft.com/en-gb/help/4020481/fix-link-exe-crashes-with-a-fatal-lnk1000-error-when-you-use-wholearch).
4. Follow the steps described [here](https://github.com/pytorch/pytorch#from-source) to build PyTorch from source.

# Verification

To ensure that PyTorch was installed correctly, you can verify the installation by running sample PyTorch code. Here you will construct a randomly initialized tensor.

First, open an Anaconda prompt via **Start &gt; Anaconda3 &gt; Anaconda Prompt**, and run `python` in it.

Then, enter the following code:

```python
from __future__ import print_function
import torch
x = torch.rand(5, 3)
print(x)
```

The output should be something similar to:

```python
tensor([[0.1935, 0.5487, 0.1230],
        [0.5119, 0.6789, 0.6307],
        [0.8938, 0.3003, 0.3712],
        [0.6285, 0.1104, 0.8474],
        [0.7535, 0.3999, 0.3722]])
```

Additionally, to check if your GPU driver and CUDA is enabled and accessible by PyTorch, run the following commands to return whether or not the CUDA driver is enabled:

```python
torch.cuda.is_available()
```