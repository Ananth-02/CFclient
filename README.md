# CFclient

Python environment for the Bitcraze Crazyflie client (cfclient 2026.8.1) on Windows.

The repo holds the pinned package list only. The virtual environment itself is not committed, since it has hard-coded local paths and is around 430 MB.

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
