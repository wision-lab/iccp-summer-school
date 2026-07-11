# Part 1: Passive Single Photon Imaging

Simulate and explore passive SPAD imaging using pre-captured photon cubes and synthetic binary frames.

**What you'll learn:**
- Recover scene flux from binary (1-bit) SPAD frames using Bernoulli statistics
- Apply tonemapping to visualize high dynamic range scenes
- Compute motion projections from photon cubes to reveal moving objects

## Quickstart

Make sure you've set up the environment at the repository root first (see [README](../README.md#setup)), then:

```bash
jupyter lab
```

Then open one of the activity notebooks below.

## Setup

Download the data files (`*.npy` and `hdr_stairs_small.exr`) from the [release page](https://github.com/wision-lab/iccp-summer-school/releases/tag/data) and place them under `data/`.

## Activities

### 1.a: High Dynamic Range Imaging → [`activity_hdr.ipynb`](activity_hdr.ipynb)

Start with a single binary frame, sum multiple frames, then invert the SPAD response to recover the scene's linear intensity. Finish by applying gamma tonemapping for display.

### 1.b: Motion Projections → [`activity_motion_projection.ipynb`](activity_motion_projection.ipynb)

Load a real photon cube of a falling die, implement shift-based motion projections to track moving objects, and build a motion sweep animation across different velocity vectors.

## Data

Pre-captured photon cubes are provided under `data/`:
- `falling_die_photon_cube.npy` — A die dropping through frame
- `traffic_photon_cube.npy` — Traffic scene (bonus)
