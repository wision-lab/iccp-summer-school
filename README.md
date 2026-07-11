# ICCP Summer School: Single Photon Imaging

Hands-on activities exploring single-photon imaging with SPAD (Single Photon Avalanche Diode) sensors.

## Setup

Create a Python virtual environment and install the dependencies.

### Option A: UV

```bash
# Install UV (if not already installed)
curl -LsSf https://astral.sh/uv/install.sh | sh

# Create a virtual environment and install dependencies
uv venv
uv pip install -r requirements.txt
```

> **Note:** This creates a virtual environment in `.venv/`. Use `uv run python ...` or `uv run jupyter lab` to run commands inside the environment, or activate the environment with `source .venv/bin/activate` (or `.venv\Scripts\activate` for windows).

### Option B: Conda / Micromamba

```bash
# Create the environment from requirements.txt
conda create -n iccp python=3.12 --file requirements.txt
conda activate iccp
```

Or with micromamba:

```bash
micromamba create -n iccp python=3.12 --file requirements.txt
micromamba activate iccp
```

### Option C: pip + venv

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Part 1: Passive Imaging ([details](part_1_passive_SPADs/README.md))

Explore passive SPAD imaging through two Jupyter notebook activities:
- **High Dynamic Range Imaging** — Recover scene flux from binary SPAD frames and apply tonemapping.
- **Motion Projections** — Use motion sweeps on photon cubes to visualize moving objects.

## Part 2: Active Imaging ([details](part_2_active_SPADs/README.md))

Use an AMS TMF8820 time-of-flight sensor with its built-in laser:
- **Activity 1** — Recreate transient histograms with different characteristics.
- **Activity 2** — Identify the laser and SPAD sensor cavities on the hardware.
- **Activity 3** — Implement your own distance estimation algorithm.