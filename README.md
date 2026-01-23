## Robust State Estimation under Sensor Faults

This repository contains an ongoing research project on robust state estimation
in distributed sensor networks under probe miscalibration and structured sensor
faults. The work is organized into clearly defined phases, with completed
experiments frozen for reproducibility and future extensions developed on top
of these baselines.

⚠️ **Project status:** Active and evolving. Additional learning-based and
fault-detection extensions are planned.

---

## Motivation

Sensor networks often rely on redundant probes and calibration to improve
measurement reliability. While calibration enforces internal probe consistency,
it is commonly assumed to provide robustness against sensor faults. This project
questions that assumption and studies how different estimation strategies behave
when calibration assumptions are violated.

---

## Completed Work (Current State)

The following components are fully implemented and frozen:

### Phase 1 — Synthetic Data Generation
- Asynchronous sensor log generation with known latent ground truth
- Probe-level gain and bias miscalibration
- Realistic noise and missingness patterns

### Phase 2 — Baseline and Calibration-Based Estimation
- Baseline averaging and temporal smoothing
- Calibration-only latent state estimation
- Analysis of probe disagreement and estimator behavior

### Phase 3 — Fault Injection and Robustness Analysis
- Controlled benign and adversarial probe-level fault injection
- Introduction of localized fault penalty metrics
- Empirical identification of calibration failure modes

### Phase 3B — Graph-Based Robustness Extension
- Deterministic graph-temporal smoothing without learning
- Sensitivity analysis of spatial coupling strength
- Demonstration of robustness–bias trade-offs

All datasets, fault scenarios, and evaluation metrics for these phases are
frozen to ensure reproducibility.

---

## Planned Extensions (Future Work)

The following extensions are planned and will build directly on the frozen
artifacts from earlier phases:

### Phase 4 — Learning-Based Robustness (GNN)
- Graph neural networks to learn corrections to calibration-only estimates
- Training on fault-injected data with consistent evaluation metrics
- Comparison against deterministic baselines

### Phase 5 — Fault Detection and Localization
- Residual-based fault indicators
- Explicit fault detection and localization models
- Transition from passive robustness to active fault tolerance

---

## Repository Structure
```
phase1_data_generation.ipynb
phase2_calibration_and_faults.ipynb
phase3_graph_robustness.ipynb
phase4_gnn_fault_robustness.ipynb # planned
artifacts/
report/
```

---

## Notes

- No fault detection or prediction is performed in the completed phases.
- No learning-based models are used prior to Phase 4.
- Ground truth is used strictly for evaluation.

---

## License

Research and educational use only.

