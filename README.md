# Cardiovascular Risk Prediction in Diabetic Patients (Exploratory Phase)

[![Python 3.10+](https://img.shields.io/badge/R-4.x-276DC3?style=flat-square&logo=r&logoColor=white)](https://www.r-project.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)
[![Evolved](https://img.shields.io/badge/Evolved_Into-cvd--diabetes--risk--ml-228B22?style=flat-square)](https://github.com/julian-borges-md/cvd-diabetes-risk-ml)
[![Published](https://img.shields.io/badge/Published-AI_in_Health_(2026)-darkgreen?style=flat-square)](https://doi.org/10.36922/AIH025490111)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0001--9929--3135-a6ce39?style=flat-square&logo=orcid)](https://orcid.org/0009-0001-9929-3135)

> **Frontier Translational Research Lab**
> Principal Investigator: Julian Borges, MD (`jyborges@bu.edu`)

## Project Lineage

This repository is the **exploratory prototype** that preceded and led to the published study. The work evolved through three stages:

| Stage | Repository | Description | Outcome |
|:---:|---|---|---|
| 1 | **This repo** (CVD-prediction-model-project) | Initial R prototype. Single train/test split, UCI Heart Failure + Diabetes datasets, logistic regression and random forest, basic downsampling. Produced the original manuscript draft and identified core clinical question. | Proof of concept |
| 2 | [cvd-diabetes-risk-ml](https://github.com/julian-borges-md/cvd-diabetes-risk-ml) | Full methodological rebuild. Migrated to leakage-resistant stratified 5-fold CV with pooled out-of-fold evaluation. SMOTE confined to training folds. McNemar's test for model comparison. SHAP analysis. FDA GMLP alignment. | Rigorous evaluation |
| 3 | [DOI: 10.36922/AIH025490111](https://doi.org/10.36922/AIH025490111) | Published in *Artificial Intelligence in Health* (AccScience Publishing, 2026). Open access. | **Published** |

## What Changed Between Stage 1 and Stage 2

| Dimension | Stage 1 (this repo) | Stage 2 (cvd-diabetes-risk-ml) |
|---|---|---|
| **Validation** | Single 80/20 train-test split | Stratified 5-fold CV, pooled OOF predictions |
| **Leakage control** | Downsampling on full dataset before split | SMOTE restricted to training folds only |
| **Model comparison** | Visual comparison of confusion matrices | McNemar's test on pooled OOF predictions |
| **Interpretability** | Feature importance plot | SHAP values, partial dependence, clinical profiles |
| **Language** | R (caret, randomForest) | R (caret, randomForest, SHAP, pROC) |
| **Reporting** | Ad hoc script + Rmd | Fully reproducible pipeline with CI (GitHub Actions) |
| **Regulatory framing** | None | FDA Good Machine Learning Practice alignment |

## Why This Repo Is Preserved

This prototype is retained to document the research lineage and methodological evolution. The progression from a single-split exploratory analysis to a leakage-resistant, CV-based evaluation with regulatory alignment demonstrates the iterative improvement process that produced the final publication.

## Contents

| File | Description |
|---|---|
| `DIA_CVD_ML RSCRIPT.R` | Original R analysis script |
| `DIA_CVD_ML SCRIPT.Rmd` | R Markdown notebook |
| `DIA_CVD_ML SCRIPT RKNIT.pdf` | Rendered analysis report |
| `DIA_CVD_ML ORIGINAL MANUSCRIPT.pdf` | Initial manuscript draft |

## Final Publication

> **"Machine Learning Insights for Cardiovascular Risk Prediction in Diabetic Patients: Emphasis on Renal and Cardiac Markers Using Random Forests"**
> Julian Borges, MD, MS
> *Artificial Intelligence in Health* (AccScience Publishing, 2026)
> DOI: [10.36922/AIH025490111](https://doi.org/10.36922/AIH025490111) | SSRN: [10.2139/ssrn.5091734](https://doi.org/10.2139/ssrn.5091734)

---

<div align="center">

**Frontier Translational Research Lab**

Department of Computer Science · Boston University · Harvard Medical School GCSRT Alumni

[![Lab Website](https://img.shields.io/badge/Lab-frontier--lab-002244?style=flat-square)](https://julian-borges-md.github.io/frontier-lab/)
[![BU CS](https://img.shields.io/badge/BU-Computer_Science-cc0000?style=flat-square)](https://www.bu.edu/cs/)
[![HMS](https://img.shields.io/badge/HMS-GCSRT_Alumni-a51c30?style=flat-square)](https://ghsm.hms.harvard.edu/education/global-clinical-scholars-research-training)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0001--9929--3135-a6ce39?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0001-9929-3135)
[![CV](https://img.shields.io/badge/Academic_CV-research--profile-4f46e5?style=flat-square)](https://julian-borges-md.github.io/research-profile/)

*Julian Borges, MD, MS · jyborges@bu.edu*

</div>
