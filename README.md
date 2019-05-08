# Project McNulty

I worked on this project at [Metis](https://www.thisismetis.com/).

### Contents
* `data/`
  * `contractor_misconduct.csv` - all data from The Project On Government Oversight's [Federal Contractor Misconduct Database](https://www.contractormisconduct.org/)
  * `clean/` - output from notebooks
    * \*`indicators`\* - with indicator dimensions
    * the rest - compact, for analysis
* `notebooks/`
  * `wrangle/`
    * `misconduct_clean.ipynb` - extract from CSV source and clean
    * `add_indicators.ipynb` - add indicators
  * `analyze/`
    * `class_correlations.ipynb` - visualize correlations between categorical features and target
    * `TSNE.ipynb`
  * `predict/`
    * `predict_disposition_type.ipynb` - survey of model performance
    * `predict_fine.ipynb` - (work in progress)
included)

### Usage
Run:
1. `misconduct_clean.ipynb`
2. `add_indicators.ipynb`
3. `disclosures_extract_clean.ipynb`
4. `add_lobbyist_features_to_misconduct.ipynb`
5. what you want from `analyze/` or `predict/`
