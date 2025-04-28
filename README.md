# Deep Metabolomics

This repository contains code used in the paper: {can add link later}

### Data

`preprocessing.py` file for some of the preprocessing steps, ignore some of the file names as it was used for all datasets, but the basic steps/ordering are the same. 

### Notebooks

All scripts contained here under the naming `{num_pipelines}_pipeline_{AD/PD}.ipynb`

Results separated by folder

# Model Training Pipelines

This repository contains several Jupyter notebooks that train, evaluate, and save machine learning models for classifying Alzheimer's/Parkinson's Disease (AD/PD) status based on provided datasets.

## Overview

Each notebook follows a consistent structure:
- **Data Loading**: 
  - Preprocessed feature and label datasets (`.csv` format) for training and testing are loaded.
- **Pipeline Construction**:
  - Pipelines are built using `pytorch's` `Module` class.
  - Each pipeline includes a standard preprocessing step (`QuantileTransformer`) followed by a machine learning classifier (Neural Network).
- **Model Training**:
  - Models are trained using the training data.
- **Evaluation**:
  - Models are evaluated on the test set using metrics such as:
    - Accuracy
    - ROC AUC score
    - Cross-Entropy Loss
    - Confusion Matrix
  - ROC curves and confusion matrices are visualized.
- **Model Saving**:
  - Trained models are saved as `.pth` files for future use.

## Outputs

For each notebook, you can expect the following outputs:
- **Trained Model Files**: `.pth` format, one per pipeline and disease type.
- **Evaluation Metrics**: Printed metrics and plots for performance visualization under `/data/`
- **Plots**:
  - Accuracy vs. Time (epochs)
  - Loss vs. Time (epochs)
  - Confusion matrices (color heatmaps)
  - ROC Curves (Receiver Operating Characteristic)

## Requirements

Key Python libraries used:
- Matplotlib
- NumPy
- Pandas
- PyTorch
- Scikit-learn

You can install the necessary packages using:

```bash
pip install matplotlib numpy pandas torch scikit-learn


-Frank
