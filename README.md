# Reproducing Figure 7A/B of "β-VAE: Learning Basic Visual Concepts with a Constrained Variational Framework" (Higgins et al., ICLR 2017)

## Requirements

Python 3.13 and an NVIDIA GPU (tested on an RTX 3080 Ti).

```
python -m pip install torch torchvision --index-url https://download.pytorch.org/whl/cu130
python -m pip install numpy pandas matplotlib ipykernel
```

Download the dSprites dataset into the same folder as the notebook:

```
curl.exe -L -o dsprites_ndarray_co1sh3sc6or40x32y32_64x64.npz https://github.com/google-deepmind/dsprites-dataset/raw/refs/heads/master/dsprites_ndarray_co1sh3sc6or40x32y32_64x64.npz
```

## How to run

1. Open `beta_vae_fig7.ipynb` in VS Code (Jupyter extension) or JupyterLab and select the Python environment above.
2. In the setup cell (Section 4), set `TRAIN_BUDGET_MIN = 110` and `GPU_BUDGET_MIN = 130`.
3. Click Run All. The figures are saved to `runs_fig7/figures/` (main figure: `fig7AB_seed0.png`).
4. If the run stops, click Run All again. Finished runs are skipped.
