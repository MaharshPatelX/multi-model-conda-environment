# Conda Environment Setup for Multi-Models or LLMs

## Installation

### Manual installation using Conda

Recommended if you have some experience with the command-line.

#### 0. Install Conda

https://docs.conda.io/en/latest/miniconda.html

#### 1. Create a new conda environment

```
conda create -n llm_env python=3.11 -y
activate llm_env
```

#### 2. Install Pytorch

| System | GPU | Command |
|--------|---------|---------|
| Linux/WSL | NVIDIA | `pip install torch torchvision torchaudio` |
| Linux/WSL | CPU only | `pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu` |
| Linux | AMD | `pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/rocm5.4.2` |
| MacOS + MPS | Any | `pip install torch torchvision torchaudio` |
| Windows | NVIDIA | `pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117` |
| Windows | CPU only | `pip install torch torchvision torchaudio` |

The up-to-date commands can be found here: https://pytorch.org/get-started/locally/. 

#### 3. Install the web UI

```
curl -o req.txt https://raw.githubusercontent.com/MaharshPatelX/conda-environment-multi-model/main/requirements.txt
pip install -r requirements.txt
```
