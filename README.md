# ForeT2F

Official repository for **ForeT2F: Enhancing Zero-Shot Prediction via Two-Stage Temporal-Frequency Pre-Training**.

## Code release status

The full implementation is being organized and will be uploaded to this repository after preparation. This repository currently provides the project description; the training and evaluation code has not yet been released. Release updates will be posted here.

## Overview

ForeT2F studies zero-shot time-series forecasting through amplitude and phase analysis and introduces a two-stage time-frequency training strategy:

1. **Stage 1:** pre-train forecasting models on source datasets using mean squared error (MSE).
2. **Stage 2:** freeze the backbone and adapt the selected prediction-head parameters with the Time-Frequency Loss (TFL), which combines MSE and the Normalized Phase Loss (NPL).

The Phase-Amplitude Loss (PAL) is a Parseval-equivalent decomposition of MSE used for analysis. NPL modifies the phase-dependent frequency weighting using normalized predicted amplitudes.

The study evaluates five forecasting architectures (PatchTST, DLinear, iTransformer, FreTS, and TiDE) and three Moirai scales. The foundation-model evaluation uses numerical time-series inputs.

## Planned release contents

- ForeT2F loss functions and two-stage training implementations.
- Model configurations and training/evaluation scripts for forecasting horizons of 96, 192, 336, and 720.
- Scripts for repeated runs, loss controls, ablations, and spectral analyses.
- Environment requirements and instructions for running the experiments.

## Paper and citation

**ForeT2F: Enhancing Zero-Shot Prediction via Two-Stage Temporal-Frequency Pre-Training**

Publication details and a BibTeX entry will be added when available.

## Acknowledgements

We acknowledge the public forecasting implementations and the time-frequency training work [FreDF](https://github.com/Master-PLC/FreDF) that informed this research. Dependencies and implementation-specific acknowledgements will accompany the code release.
