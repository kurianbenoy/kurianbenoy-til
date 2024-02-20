# Installing software in E2E cloud compute

Most of the instances in E2E cloud comes with Python, but not with pip. CUDA drivers are install, but pytorch or tensorflow is missing.\
\


```
apt-get install python3-pip
```

Check CUDA version:\
\


```
nvcc --version
```

Then install pytorch for cuda:

```
python3 -m pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
```

Verify the installation using:\
\


```
import torch
torch.cuda.is_available()
```
