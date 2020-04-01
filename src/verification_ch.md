# 验证

我们可以通过运行 PyTorch 的示例代码来验证是否正确安装了 PyTorch。这里我们将构造一个随机初始化的 tensor。

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