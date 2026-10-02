# Reproducibility_Exercise
Reproducibility Exercise Assignment for Week 2 for Programming for HDS

Purpose
A reproducible Jupyter notebook that explores how patient measurements  relate to a diabetes diagnosis. It is written so that a data science team at another clinical site can run it start to finish and reproduce the results. 

Project Contents
Reproducibility_Exercise/
├── starter_diabetes_risk_factor_analysis.ipynb          # analysis notebook
├── requirements.txt                  # required packages and versions
├── README.md                         # this file 
|── Example_Dataset_Diabetes.csv      # example dataset
|── starter_diabetes_risk_factor_analysis.ipynb #google collab notebook

Required Software and Libraries
Python 3.11 or newer 
Jupyter (JupyterLab, VS Code, or similar)
pandas, numpy, scipy, matplotlib (exact versions in requirements.txt)

Installation and Setup
Download the repository (Code → Download ZIP, then unzip) or clone it:
bash
   git clone https://github.com/sudiksharamakrishnanhse-lab/Reproducibility_Exercise
   cd Reproducibility_Exercise

How to Run the Notebook
Open the notebook from the project folder. In VS Code, use File → Open Folder and select the project folder. 
Select the Python environment as the notebook kernel.
Choose Restart and Run All. No manual edits are needed, and it runs in about a minute.

Dataset Requirements
Included file: Example_Dataset_Diabetes.csv, with 768 rows and 9 numeric columns. Downloading the repository includes it, so the dataset does not need to be obtained separately. 
Columns: Pregnancies, Glucose (mg/dL), D_BP (diastolic blood pressure, mm Hg), Skin_Thickness (mm), Insulin (µU/mL), BMI (kg/m²), Pedigree (diabetes pedigree function), Age (years), Outcome (0 = no diabetes, 1 = diabetes).

Expected Outputs
Running the notebook should produce:
Descriptive statistics by outcome (mean glucose about 110.6 mg/dL without diabetes and 142.3 mg/dL with diabetes)
Histograms, a glucose box plot, a BMI-vs-glucose scatter plot, and a Spearman correlation heatmap (Glucose–Outcome ρ ≈ 0.48)
t-test of glucose by outcome: t ≈ −15.70, p ≈ 2.5 × 10⁻⁴⁸
Mann-Whitney U test: U = 27,393.5, p ≈ 1.3 × 10⁻⁴⁰
Seeded sample and bootstrap (SEED = 42) that are identical on every run

Assumptions and Limitations
Zeros are treated as missing. Zeros in Glucose, D_BP, Skin_Thickness, Insulin, and BMI are not physically possible, so they are converted to missing values. Confirm how zeros are recorded before using other data.
Association, not causation. Results describe relationships in the data and no predictive model is built or validated.
One population. The example data come from one specific group, so results at another site may differ.
