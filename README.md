# CFclient

Python environment for the Bitcraze Crazyflie client (cfclient 2026.8.1) on Windows.

The repo holds the full virtual environment (Include, Lib, Scripts, pyvenv.cfg) and the pinned package list. The venv has hard-coded paths, so it only runs as is from C:\cfclient-env311 with the same uv Python install. On any other PC, rebuild it from requirements.txt as below.

## Setup

- Python 3.11 (tested with 3.11.15, installed through uv)
- Windows x64

```powershell
uv python install 3.11
uv venv --python 3.11 C:\cfclient-env311
C:\cfclient-env311\Scripts\activate
uv pip install -r requirements.txt
```

Without uv:

```powershell
py -3.11 -m venv C:\cfclient-env311
C:\cfclient-env311\Scripts\activate
pip install -r requirements.txt
```

## Run

```powershell
cfclient
```

Other tools installed with it: `cfheadless`, `cfloader`, `cfzmq`.

## Main packages

- cfclient 2026.8.1
- cflib 0.1.34
- PyQt6 6.7.1
- numpy 2.4.6, scipy 1.17.1
- pyqtgraph 0.14.0, vispy 0.16.2
