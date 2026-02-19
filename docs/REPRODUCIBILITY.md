# Reproducibility Guide (DATGR)

## Google Colab Execution (Recommended)

The experiments were executed using Google Colab (Python 3.10 runtime).

No local installation is required.

---

## Step 1: Open the Notebook

Open `DATGR.ipynb` directly in Google Colab.

The file is available here:

https://github.com/sahanakv01123/DATGR/

---

## Step 2: Runtime Configuration

- Runtime → Change runtime type
- Hardware accelerator: None (CPU sufficient)
- Python version: Default (3.10+)

GPU is optional and only speeds up sentence embeddings.

---

## Step 3: Install Dependencies

The first notebook cell installs all required packages automatically.

No additional setup is required.

---

## Step 4: Run All Cells

Runtime → Run all

Expected output:
- AUROC/AUPRC results table
- fig_auroc.png
- fig_auprc.png
- fig_edits.png

---

## Notes on Variability

Minor metric variation (±0.01–0.03) may occur due to:
- Node2Vec random walks
- Hard negative sampling
- Probability calibration

However, qualitative results remain stable.
