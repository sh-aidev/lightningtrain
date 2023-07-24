<div align="center">

# LightningTrain

[![python](https://img.shields.io/badge/-Python_%7C_3.10-blue?logo=python&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![pytorch](https://img.shields.io/badge/PyTorch_2.0+-ee4c2c?logo=pytorch&logoColor=white)](https://pytorch.org/get-started/locally/)
[![lightning](https://img.shields.io/badge/-Lightning_2.0+-792ee5?logo=pytorchlightning&logoColor=white)](https://pytorchlightning.ai/)
[![hydra](https://img.shields.io/badge/Config-Hydra_1.3-89b8cd)](https://hydra.cc/)

A clean and simple PyTorch Lightning + Hydra projects.

</div>

## 📌  Introduction

This repository contains a simple PyTorch Lightning + Hydra project template. It is designed to be a starting point for your own projects. It is based on the [PyTorch Lightning](https://lightning.ai/docs/pytorch/stable/).

<br>

## 📦  Main Technologies

[PyTorch Lightning](https://github.com/PyTorchLightning/pytorch-lightning) - a lightweight PyTorch wrapper for high-performance AI research. Think of it as a framework for organizing your PyTorch code.

[Hydra](https://github.com/facebookresearch/hydra) - a framework for elegantly configuring complex applications. The key feature is the ability to dynamically create a hierarchical configuration by composition and override it through config files and the command line.

<br>

## 📁  Project Structure

The directory structure of new project looks like this:

```
configs
│   ├── data                     <- Data configs
configs
│   ├── hydra                    <- Hydra configs
│   ├── local                    <- Local configs
│   ├── model                    <- Model configs
│   ├── paths                    <- Project paths configs
│   ├── trainer                  <- Trainer configs
│   ├── eval.yaml             <- Main config for evaluation
│   └── train.yaml            <- Main config for training
│
├── data                   <- Project data
│
├── logs                   <- Logs generated by hydra and lightning loggers
│
├── notebooks              <- Jupyter notebooks. Naming convention is a number (for ordering),
│                             the creator's initials, and a short `-` 
│
├── lightningtrain                    <- Source code
│   ├── data                     <- Data scripts
│   ├── models                   <- Model scripts
│   ├── utils                    <- Utility scripts
│   │
│   ├── eval.py                  <- Run evaluation
│   └── train.py                 <- Run training
│
├── tests                  <- Tests of any kind
│
├── .gitignore                <- List of files ignored by git
├── .project-root             <- File for inferring the position of project root directory
├── Makefile                  <- Makefile with commands like `make train` or `make test`
├── pyproject.toml            <- Configuration options for testing and linting
├── requirements.txt          <- File for installing python dependencies
├── setup.py                  <- File for installing project as a package
└── README.md
```

<br>

## 🚀  Quickstart
```bash
# clone project
git clone https://github.com/dlwizard/lightningtrain.git
cd lightningtrain

# create docker container with .devcontainer.json
# or install dependencies locally

# install project as a package
pip install -e .

# run training
lightningtrain_train data.num_workers=16

# run evaluation
lightningtrain_eval data.num_workers=16

```

## 📝  Docker container usage instructions
**Prerequisites:**
- [Docker](https://docs.docker.com/get-docker/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension

**Steps:**
1. Clone this repository
2. Open the repository in Visual Studio Code
3. press crtl+shift+p and select "Remote-Containers: Reopen in Container"
4. Wait for the container to build
5. Open a terminal in Visual Studio Code and run the following commands:
```
# install project as a package
pip install -e .

# run training
lightningtrain_train data.num_workers=16

# run evaluation
lightningtrain_eval data.num_workers=16

```

<br>

## 📝 Instructions for PyPi package usage
**Prerequisites:**
- [Python 3.10](https://www.python.org/downloads/release/python-3100/)
- [pip](https://pip.pypa.io/en/stable/installation/)
- [virtualenv](https://virtualenv.pypa.io/en/latest/installation.html)

**Steps:**
1. python -m venv venv
2. source venv\Scripts\activate
3. python3 -m pip install lightningtrain
4. lightningtrain_train data.num_workers=16
5. lightningtrain_eval data.num_workers=16

<br>


## References
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/stable/)
- [Hydra](https://hydra.cc/docs/intro/)
- [Lightning-Hydra-Template](https://github.com/ashleve/lightning-hydra-template.git)
- [Lightning Template](https://github.com/satyajitghana/lightning-template.git)

<br>