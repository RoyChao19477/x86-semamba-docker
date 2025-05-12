# x86 SEMamba Docker Image

This Docker image provides a pre-configured development environment for running [SEMamba](https://github.com/RoyChao19477/SEMamba) models on x86 systems with NVIDIA GPUs like A100, RTX 4090, RTX 3090, or any CUDA-compatible hardware. It contains Python 3.12 and PyTorch 2.2.2, built on top of Ubuntu 22.04 with CUDA 12.4.

---

## Contents

- **OS**: Ubuntu 22.04 (x86_64)
- **Python**: 3.12 (via Miniconda)
- **CUDA**: 12.4 (base image)
- **PyTorch**: 2.2.2
- **TorchVision**: 0.17.2
- **TorchAudio**: 2.2.2
- **Mamba-SSM**: 1.2.0
- **Essential packages**: git, vim, screen, htop, tmux, openssh, etc.

---

## Usage

### Option 1: Pull from GHCR (Recommended)

```bash
docker pull ghcr.io/roychao19477/x86_semamba_py312_pt222_cuda124:latest

docker run --gpus all -it -v $(pwd):/workspace ghcr.io/roychao19477/x86_semamba_py312_pt222_cuda124:latest
```

### Option 2: Load from Hugging Face `.tar`

#### Download Docker Image

```bash
wget https://huggingface.co/datasets/rc19477/x86-semamba-docker/resolve/main/x86_semamba_py312_pt222_cuda124.tar
```

#### Load Docker Image

```bash
docker load < x86_semamba_py312_pt222_cuda124.tar
```

#### Run Container

```bash
docker run --gpus all -it -v $(pwd):/workspace x86_semamba_py312_pt222_cuda124
```

---

## Purpose

- Simplifies setup for SEMamba on x86 GPU systems
- Provides reproducible environment with version-pinned core libraries

---

## License & Attribution

- This Docker image is shared for **non-commercial research purposes**.
- All included libraries retain their original licenses.
- Based on [PyTorch](https://pytorch.org/), [Miniconda](https://docs.conda.io/en/latest/miniconda.html), and [Mamba](https://github.com/state-spaces/mamba).

---

## Maintainer

For questions or issues, feel free to open a discussion or connect via GitHub.
