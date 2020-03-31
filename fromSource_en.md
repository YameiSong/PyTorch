# Building From Source

For the majority of PyTorch users, installing from a pre-built binary via a package manager will provide the best experience. However, there are times when you may want to install the bleeding edge PyTorch code, whether for testing or actual development on the PyTorch core. To install the latest PyTorch code, you will need to build PyTorch from source.

## Prerequisites

1. Install [Anaconda](install_en.md/#anaconda).
2. Install [CUDA](https://developer.nvidia.com/cuda-downloads), if your machine has a [CUDA-enabled GPU](https://developer.nvidia.com/cuda-gpus).
3. If you want to build on Windows, Visual Studio 2017 14.11 toolset and NVTX are also needed. Especially, for CUDA 8 build on Windows, there will be an additional requirement for VS 2015 Update 3 and a patch for it. The details of the patch can be found out [here](https://support.microsoft.com/en-gb/help/4020481/fix-link-exe-crashes-with-a-fatal-lnk1000-error-when-you-use-wholearch).
4. Follow the steps described [here](https://github.com/pytorch/pytorch#from-source) to build PyTorch from source.