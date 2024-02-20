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

Install jupyter lab and run with no password:

```
pip install jupyterlab

jupyter lab --allow-root --ip='*' --NotebookApp.token='' --NotebookApp.password=''
```



Then expose URL with ngrok: `ngrok http 8888`\
\


