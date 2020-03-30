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
| | |
|-|-|
| _**NOTE**_ | To check your Python version, run `py` in Windows PowerShell. |

## Package Manager

To install the PyTorch binaries, you will need to use at least one of two supported package managers: [Anaconda](https://www.anaconda.com/distribution/#windows) and [pip](https://pypi.org/project/pip/). Anaconda is the recommended package manager as it will provide you all of the PyTorch dependencies in one, sandboxed installation, including Python and pip.

### Anaconda

To install Anaconda: 

1. On the [Anaconda](https://www.anaconda.com/distribution/#windows) website, download the 64-bit graphical installer.
2. Run the installer, and then apply all default options to install Anaconda.

### pip

If you installed Python by any of the recommended ways above, [pip](https://pypi.org/project/pip/) will have already been installed for you.
