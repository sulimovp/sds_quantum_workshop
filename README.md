# SDS2026 — Quantum AI: From Inspiration to Enhancement - A Practical Journey

All examples run on a laptop with CPU simulators; no quantum hardware is needed.

## Installation

Use Python 3.11 or 3.12. The commands below assume that you start in the
workshop folder.

### Windows PowerShell

```powershell
py -3.11 -m venv quantum_env
.\quantum_env\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter notebook
```

If PowerShell blocks activation, run:

```powershell
Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
```

Then activate the environment again.

### macOS

```bash
python3 -m venv quantum_env
source quantum_env/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter notebook
```

If `python3` points to an old Python version, install a current Python from
[python.org](https://www.python.org/downloads/) or use Homebrew:

```bash
brew install python
```

### Linux

```bash
python3 -m venv quantum_env
source quantum_env/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter notebook
```

On Debian or Ubuntu, install the virtual-environment package first if needed:

```bash
sudo apt update
sudo apt install python3-venv
```

## Running The Notebooks

Start Jupyter from the workshop folder:

```bash
jupyter notebook
```

Open the notebooks in `notebooks/story/` in numerical order. If a notebook asks
for a kernel, choose the kernel from the `quantum_env` environment.

## Checking The Setup

After installation, run this in a notebook cell:

```python
import pennylane as qml
import qiskit
import torch

print("PennyLane:", qml.__version__)
print("Qiskit:", qiskit.__version__)
print("PyTorch:", torch.__version__)
```

The workshop targets PennyLane `>=0.44`, Qiskit `>=2.2`, and PyTorch `>=2.5`.

## Troubleshooting

If `pip install -r requirements.txt` fails, first upgrade `pip`:

```bash
python -m pip install --upgrade pip setuptools wheel
```

If Jupyter does not show the environment, install the kernel manually:

```bash
python -m ipykernel install --user --name quantum_env --display-name "Python (quantum_env)"
```

If a notebook kernel dies on Windows during numerical code, restart Jupyter from
the activated `quantum_env` terminal and rerun the notebook from the top.

## Authors

Dr. Pavel Sulimov, Claude Lehmann
