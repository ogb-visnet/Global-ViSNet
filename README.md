# Global-ViSNet

This repository is the official implementation of Global-ViSNet, based on the official implementation of [Transformer-M](https://github.com/lsj2408/Transformer-M.git).

## Installation

- Clone this repository

```shell
git clone https://github.com/ogb-visnet/Global-ViSNet.git
```

- Install the dependencies (Using [Anaconda](https://www.anaconda.com/), tested with CUDA version 11.0)

```shell
cd ./Global-ViSNet
conda env create -f requirement.yaml
conda activate Global-ViSNet
pip install torch==1.7.1+cu110 torchvision==0.8.2+cu110 torchaudio==0.7.2 -f https://download.pytorch.org/whl/torch_stable.html
pip install torch_geometric==1.6.3 torch_scatter==2.0.7 torch_sparse==0.6.9 -f https://data.pyg.org/whl/torch-1.7.1+cu110.html
pip install azureml-defaults
pip install rdkit-pypi cython
python setup.py build_ext --inplace
python setup_cython.py build_ext --inplace
pip install -e .
pip install --upgrade protobuf==3.20.1
pip install --upgrade tensorboard==2.9.1
pip install --upgrade tensorboardX==2.5.1
```