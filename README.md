# CECS 553 — Machine Vision (Colab Notebooks)

This repository holds Google Colab notebooks and supporting files for the CECS 553 Machine Vision course. Notebooks are intended to be opened and run in Google Colab for easy GPU access and environment reproducibility.

## Quick start — open a notebook in Colab

There are two simple ways to open a notebook in Colab:

- Use the Colab "Open notebook" dialog and paste the GitHub URL to the notebook.
- Add an "Open in Colab" badge to any notebook README or the notebook itself. Example badge Markdown (replace the path with the correct notebook path):

```
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nhefner12/CECS_553_Labs/blob/main/notebooks/NN_01_intro.ipynb)
```

If your notebook requires files from `data/` or `assets/`, upload them to your Google Drive and mount the drive in Colab, or create download links from a cloud storage provider.

## Recommended repository layout

Use a predictable structure so students and collaborators can find notebooks and data quickly:

```
.
├─ notebooks/           # All .ipynb files (numbered + descriptive names)
├─ data/                # Small example datasets (do NOT commit large raw datasets)
├─ assets/              # Images, plots, model weights, etc.
├─ requirements.txt     # Optional: pip-installable dependencies
└─ README.md
```

Naming suggestion for notebooks: `NN_<lesson#>_<short-topic>.ipynb`, e.g. `NN_01_image_io.ipynb`.

## Dependencies

For easy Colab usage you typically don't need to pin everything — Colab already installs many common libraries. Still, having a `requirements.txt` helps when running locally.

Typical packages for the course:

```
numpy
scipy
matplotlib
opencv-python
scikit-image
torch         # optional, only if using PyTorch
torchvision   # optional
```

Create a `requirements.txt` with the packages you need and install locally with:

```powershell
# create a venv (Windows PowerShell)
python -m venv .venv; .\\.venv\\Scripts\\Activate.ps1; python -m pip install -r requirements.txt
```

In Colab, install any extra packages at the top of a notebook with `!pip install -r requirements.txt` or `!pip install package-name`.

## Running notebooks locally

To run notebooks on your machine, install Jupyter and the required packages:

```powershell
python -m pip install --upgrade pip; python -m pip install jupyterlab
jupyter lab
# or
jupyter notebook
```

## Contributing guidelines (suggested)

- Add notebooks under `notebooks/`.
- Keep notebooks focused and add a short description in the first markdown cell.
- If a notebook depends on a dataset, include a small sample in `data/` or provide a download script that places files into `data/`.
- Consider adding an "Open in Colab" badge at the top of important notebooks.

## Next steps

- Add a `requirements.txt` for reproducibility.
- Add an example notebook `notebooks/NN_01_intro.ipynb` demonstrating image I/O and visualization.
- (Optional) Add CI checks that ensure notebooks run (e.g. using nbval or papermill for smoke tests).

---

If you'd like, I can:

- Add a starter `requirements.txt` with common CV libraries.
- Create a small example notebook template and place it under `notebooks/`.

Feel free to tell me which of those you'd like next.

