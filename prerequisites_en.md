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

To upgrade GPU driver:

1. Right-click on the Windows desktop and click **NVIDIA Control Panel.**
2. Navigate to the **Help** menu and click **Updates.**
3. In the **Updates** tab, click **Check for Updates.**
4. Follow the instructions from NVIDIA to upgrade your GPU driver to the latest version.