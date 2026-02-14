# Data Engineering Foundations — Titanic (Kaggle)

This repo tracks my Data Engineering Foundations practice using the Kaggle Titanic dataset.

## Current Status
- Dataset: Titanic (train/test)
- Stage: Cleaning + Feature Engineering (Notebook: DM_DAY_01.ipynb)

## Completed
- Target identified: `Survived` (train only)
- Train/Test separated properly
- Missing values handled (fit on train, applied to test):
  - `Embarked`: filled with train mode
  - `Age`: filled using group-median by (`Pclass`, `Sex`) + fallback median
  - `Cabin`: extracted `Deck`, filled missing as `Unknown`, dropped `Cabin`
  - `Fare` (test): filled with train median
- Feature engineering:
  - `Title` extracted from `Name`
  - Rare titles grouped into `Rare`, `Miss`, `Mrs`

## Next Steps
- Encode categorical variables (OneHotEncoding)
- Build a sklearn pipeline (preprocess + model)
- Baseline model + cross-validation
- Improve features (FamilySize, IsAlone, etc.)

## How to run
1. Create environment and install:
   - `pip install -r requirements.txt`
2. Open notebook `DM_DAY_01.ipynb` in Jupyter.
