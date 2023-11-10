# Quantum Optimization Toolkit

![Tests](https://github.com/jpmorganchase/QOKit/actions/workflows/qokit-package.yml/badge.svg)
[![arXiv](https://img.shields.io/badge/arXiv-2309.04841-b31b1b.svg?style=plastic)](https://arxiv.org/abs/2309.04841)
[![PyPi version](https://badgen.net/pypi/v/qokit)](https://pypi.org/project/qokit/)
[![PyPI download month](https://img.shields.io/pypi/dm/qokit.svg)](https://pypi.org/project/qokit/)
[![PyPI pyversions](https://img.shields.io/pypi/pyversions/qokit.svg)](https://pypi.org/project/qokit/)
[![PyPI license](https://img.shields.io/pypi/l/qokit.svg)](https://pypi.org/project/qokit/)

This repository contains fast CPU and GPU simulators for benchmarking the Quantum Approximate Optimization Algorithm, as well as scripts for generating matching quantum circuits for execution on hardware. See the [examples](./examples) folder for a demo of this package.

### Install

Creating a virtual environment is recommended before installing.
```
python -m venv qokit
source qokit/bin/activate
pip install -U pip
```

Install requires `python>=3.9` and `pip >= 23`. It is recommended to update your pip using `pip install --upgrade pip` before install.

```
git clone https://github.com/jpmorganchase/QOKit.git
cd QOKit/
pip install -e .
```

Some optional parts of the package require additional dependencies. 
- Using commercial IP solvers to solve optimizations problems: `pip install qokit[solvers]`
- GPU simulation: `pip install qokit[GPU]`
- Development: `pip install qokit[dev]`


If compilation fails, try installing just the Python version using `QOKIT_PYTHON_ONLY=1 pip install -e .`.

Installation can be verified by running tests using `pytest`.

#### MaxCut

For MaxCut, the datasets in `qokit/assets/maxcut_datasets` must be inflated
