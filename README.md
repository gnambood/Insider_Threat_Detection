# Insider Threat Detection

Machine learning experiments on employee activity data for insider-threat classification.

This repository currently contains a Jupyter notebook, `threat_detection.ipynb`, and monthly CSV data files. It is an **experimental analysis**, not a deployed monitoring or security product.

## What is included

- A notebook containing data preparation, modelling and evaluation work
- Monthly CSV files from December 2009 through May 2011
- The historical experiments preserved in their existing format

## Research question

Can patterns in employee activity help distinguish potentially suspicious behaviour from routine activity using supervised classification?

The work investigates this question in a research setting. Its outputs should not be interpreted as a validated production threat-detection system.

## Inspecting the work

1. Open [`threat_detection.ipynb`](threat_detection.ipynb) to review the experiment.
2. Review its input paths and dataset assumptions before attempting to execute it.
3. Use a separate Python environment when installing any notebook dependencies.
4. Do not treat previously saved notebook outputs as independently reproduced results.

There is not yet a documented, tested one-command reproduction workflow in this repository.

## Evaluation notes

An earlier project summary reports **99.23% accuracy and 0.97 macro-F1** for Random Forest. Those numbers are **not presented here as independently verified test performance** until the underlying notebook's data split, evaluation unit, class balance and leakage controls have been audited.

Before promoting this repository as portfolio evidence, document:

- The exact dataset source and version, and whether any records are synthetic
- What one prediction represents (event, employee, session or another unit)
- Train/validation/test separation and whether people or time periods overlap
- Preprocessing and feature construction order relative to the split
- Minority-class precision/recall and the confusion matrix
- Dependency versions and a clean reproduction procedure

## Current limitations

This is a notebook-oriented project, with datasets committed alongside analysis rather than provided through a small reproducible pipeline. A future cleanup should separate source data, experiments, and generated outputs without changing the original methodology or silently rewriting historical results.

## Repository status

**Documentation cleanup in progress.** The notebook and data have been left unchanged pending a separate technical audit.
