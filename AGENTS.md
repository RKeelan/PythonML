# AGENTS.md

This file provides guidance to AI coding agents working in this repository.

## Project Overview

Educational repository recreating neural network architectures from scratch using PyTorch. Each file is a standalone implementation of a specific architecture or technique — there is no shared framework or library structure beyond the `Diffusion/` package.

## Setup

```bash
pip install -r requirements.txt
```

Python 3.12 is used in CI.

## Running Scripts

Scripts are standalone and typically run directly:

```bash
python train_gpt2.py
python char_gpt.py
python diffusion.py
python lenet.py
```

Notebooks (`.ipynb`) are used for some implementations (MLP, backprop, GPT-2 exploration, WaveNet, tokenizer).

## Architecture

- **Standalone scripts**: Each `.py` file at the root is a self-contained implementation of a model (GPT-2, character-level GPT, LeNet, UNet, diffusion, bigram/MLP for makemore, movie recommendations)
- **`Diffusion/`**: The only shared package — contains `simple_unet.py` (SimpleUNet model) and `utils.py` (BasicDataset), imported by `diffusion.py`
- **`Images/`**: Static image assets used by some scripts
- **`data/`**, **`checkpoints/`**, **`wandb/`**: Gitignored directories for datasets, model checkpoints, and experiment tracking

## CI

GitHub Actions runs on push/PR to main: checks out code, sets up Python 3.12, and installs dependencies. There are no tests or linting configured.
