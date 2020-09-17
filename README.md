physionet 2012: in-hospital death prediction
================
Xiangnan Dang
9/16/2020

### key parts

  - data import, transform, and feature extraction:
    R/1\_physionet\_preprocessing.Rmd and
    R/1\_physionet\_preprocessing.html
  - intermediate dataframes (.csv) and EDA (.html, auto processed using
    pandas\_profiling): proData/

df\_gd: general descriptor; df\_gd\_ro: remove outlier; df\_ts: time
series variables; df\_ts\_ro: remove outlier; df\_ts\_agg: feature
extraction by aggregation with min, max, median

  - modeling: Py/ with six model iteration

model1: base result with minimum consideration

model2: fix imbalanced label

model3: fix multicollinearity

model4: fix variable with normalization and transformation

model5: combining fix imbalanced label, fix multicollinearity and
normalization / transformation

model6: additional exploration on feature variable binning /
categorization

### other parts

  - R package control: packrat/
  - Python package control: requirements.txt and venv\_physionet/
  - source data from physionet: srcData/
