# Feature Importance Analysis for One-Shot Percussive Sound Classification

This repository contains the extracted feature matrix and analysis notebooks used in the study on one-shot percussive sound classification, gradient-based feature importance, feature reduction, and embedding-space analysis.

## Repository Structure

```text
.
├── data/
│   └── one_shot_features_clean_V4.csv
├── notebooks/
│   ├── train_42feats_multirun.ipynb
│   ├── train_20feats_multirun.ipynb
│   ├── train_10feats_multirun.ipynb
│   ├── feature_importance_5model.ipynb
│   └── embedding_space_analysis_raw_vs_ann.ipynb
├── README.md
├── requirements.txt
└── LICENSE
```

## Repository Contents

### Data

- `data/one_shot_features_clean_V4.csv`  
  Extracted feature-level dataset containing 42 hand-crafted audio features and class labels for 6,435 one-shot percussive audio samples.

### Notebooks

- `notebooks/train_42feats_multirun.ipynb`  
  Trains the artificial neural network using the full 42-feature representation across multiple independent runs.

- `notebooks/train_20feats_multirun.ipynb`  
  Trains the same network architecture using the top 20 features selected according to gradient-based feature importance.

- `notebooks/train_10feats_multirun.ipynb`  
  Trains the same network architecture using the top 10 features selected according to gradient-based feature importance.

- `notebooks/feature_importance_5model.ipynb`  
  Performs gradient-based feature importance analysis across five independently trained full-feature models.

- `notebooks/embedding_space_analysis_raw_vs_ann.ipynb`  
  Compares the raw hand-crafted feature space with the learned ANN embedding space using clustering and retrieval-based metrics.

## Data Availability

The original raw audio files are not included in this repository due to licensing restrictions associated with the source materials. Instead, this repository provides the extracted numerical feature matrix and class labels required to reproduce the classification, feature-importance, feature-reduction, and embedding-space analyses reported in the accompanying paper.

The provided CSV file contains feature-level data only. It does not include or redistribute any raw audio recordings.

## Requirements

The main Python libraries used in the experiments are listed in `requirements.txt`.

To install the dependencies, run:

```bash
pip install -r requirements.txt
```

## Reproducibility Notes

The notebooks are intended to be run from the `notebooks/` directory. The feature matrix is expected to be located at:

```text
../data/one_shot_features_clean_V4.csv
```

For reproducibility, the experiments use fixed train-validation splits where applicable and repeat model training across multiple random seeds.

## Citation

If you use this repository, please cite the accompanying paper.

```bibtex
@article{pasa_one_shot_feature_importance,
  title   = {Feature Importance Analysis for One-Shot Percussive Sound Classification},
  author  = {Pasa, Can},
  journal = {To be updated},
  year    = {To be updated}
}
```

## License

The analysis code in this repository is released under the MIT License. The feature-level dataset is provided for research and reproducibility purposes only. The original raw audio materials are not redistributed.
