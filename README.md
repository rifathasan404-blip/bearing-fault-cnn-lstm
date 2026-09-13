# Bearing Fault Diagnosis Using Multi-Scale CNN-LSTM

## Objective

This thesis investigates bearing fault diagnosis using a multi-scale
CNN-LSTM deep learning model applied to the Case Western Reserve University
bearing dataset.

## Current status

- CWRU recordings downloaded and validated
- Drive-end signals identified
- Initial data inspection in progress
- Multi-scale CNN-LSTM architecture not yet trained

## Dataset

The current recordings are:

| File | Class |
|---|---|
| 97.mat | Normal |
| 105.mat | Inner-race fault |
| 118.mat | Ball fault |
| 130.mat | Outer-race fault |

Raw `.mat` files are intentionally not tracked in Git because they are
large binary files. See `data/README.md` for provenance and download
instructions.

## Planned experiments

1. Inspect signals
2. Segment signals into windows
3. Train a baseline 1D CNN
4. Train a single-scale CNN-LSTM
5. Train the proposed multi-scale CNN-LSTM
6. Perform ablation and robustness experiments
7. Evaluate with accuracy, precision, recall, F1-score, and confusion matrix

## Reproducibility

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
