# ElevateLabs-TASK-4
Breast Cancer Detection 

## Overview
This project builds a binary classifier using **Logistic Regression** to predict whether a tumor is **malignant (M)** or **benign (B)** based on the Breast Cancer Wisconsin dataset.


## Common Errors & Fixes
- **Error: `ValueError: Input X contains NaN`**
  - Cause: Dataset has missing values.
  - Fix: Use `SimpleImputer(strategy='mean')` to replace NaNs with column means.

- **Error: `ValueError: With n_samples=0...`**
  - Cause: Dropping rows with NaN removed all samples, leaving dataset empty.
  - Fix: Do not drop all rows. Instead, impute missing values before splitting.
