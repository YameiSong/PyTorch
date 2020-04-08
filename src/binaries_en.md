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