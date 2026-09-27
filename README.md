Molecular-LogP-Prediction

A small ML project predicting experimental lipophilicity (LogD) of drug-like molecules from their structure, using RDKit descriptors and regression models.
What it does

Parses and validates molecule SMILES strings with RDKit.

Computes 9 molecular descriptors (MolWt, TPSA, HBD, HBA, RotatableBonds, RingCount, HeavyAtomCount, FractionCSP3, NumAromaticRings). RDKit's own LogP is excluded from modeling — it's a proxy for the target itself.

Compares 5 regression models (Linear, Polynomial, SVR, Decision Tree, Random Forest), tunes Random Forest with GridSearchCV, and validates with 5-fold cross-validation.
Interprets the best model with feature importance, PCA, and error analysis.

Setup

pip install pandas numpy matplotlib seaborn rdkit scikit-learn

Usage

Open the notebook in Google Colab and run top to bottom.

Dataset

Lipophilicity (ChEMBL, ~4200 molecules).
