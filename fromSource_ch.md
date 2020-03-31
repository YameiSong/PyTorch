# 通过源代码安装

对于大多数 PyTorch 用户来说，通过程序包管理器安装预先构建的二进制文件是最佳的选择。但是，有时出于测试或者开发需求，你可能需要安装最新的 PyTorch 代码。对于情况，你可以从源代码构建 PyTorch。

## 前期准备

1. 安装 [Anaconda](install_en.md#anaconda-1)。
2. 如果你的机器安装了[支持 CUDA 功能的 GPU]((https://developer.nvidia.com/cuda-gpus))，请下载并安装 [CUDA](https://developer.nvidia.com/cuda-downloads)。
3. 若要在 Windows 上构建 PyTorch，你还需要安装 Visual Studio 2017 14.11 工具集和 NVTX。尤其对于构建在 Windows 上的 CUDA 8 而言，你需要额外安装 VS 2015 Update 3 和一个补丁。你可以在[这里]((https://support.microsoft.com/en-gb/help/4020481/fix-link-exe-crashes-with-a-fatal-lnk1000-error-when-you-use-wholearch))查看补丁的详细信息。
4. 按照[这里](https://github.com/pytorch/pytorch#from-source)描述的步骤，从源代码构建 PyTorch。