# Drift-Aware Temporal Graph Rewiring (DATGR) for Adaptive Semantic Modeling in Biomedical Text

This repository contains the official implementation of **DATGR**, a drift-aware framework for modeling temporal semantic evolution in biomedical text through lightweight graph rewiring.

The implementation reproduces the experimental results reported in:

> Drift-Aware Temporal Graph Rewiring (DATGR) for Adaptive Semantic Modeling in Biomedical Text  
> Accepted at IEEE CAI 2026

---

## Overview

DATGR introduces an edge-centric temporal adaptation mechanism that:

- Models semantic drift via transformer-based embeddings
- Updates co-occurrence graph structure using a logistic rewiring rule
- Avoids expensive embedding retraining
- Improves link-prediction AUROC while maintaining stable precision-recall behavior

---

## Quick Start (Google Colab - Recommended)

Run the experiments directly in Google Colab:

1. Open `DATGR.ipynb`
2. Runtime → Run All
3. Results and figures will be generated automatically

No local installation is required.

---

## What the Notebook Produces

Running the notebook will:

- Download the BIOMRC dataset (`nlpaueb/BIOMRC`)
- Construct temporal co-occurrence graphs
- Compute semantic drift
- Perform drift-aware graph rewiring (DATGR)
- Evaluate link prediction performance
- Generate:
  - `fig_auroc.png`
  - `fig_auprc.png`
  - `fig_edits.png`
  - AUROC/AUPRC results table

---

## Experimental Configuration

Default parameters used in the paper:

- Abstracts: 2000
- Temporal windows: 4–5
- Vocabulary size per window: 400 terms
- Node2Vec: 64 dimensions
- Rewiring rate (η): 0.2
- Logistic coefficients: (0, 3, 2, 1)
- Top-k sparsification: 5

Minor metric variation (±0.01–0.03) may occur due to stochastic components.

---

## Dataset

- BIOMRC (Biomedical Reading Comprehension Dataset)
- Automatically downloaded via Hugging Face `datasets`

---

## Reproducibility

See `REPRODUCIBILITY.md` for detailed execution instructions.

---

## Citation

If you use this code, please cite:

```bibtex
@inproceedings{datgr2026,
  title={Drift-Aware Temporal Graph Rewiring for Biomedical Semantic Evolution},
  author={Vijayakumar, B and others},
  booktitle={IEEE Conference on Artificial Intelligence (CAI)},
  year={2026}
}
