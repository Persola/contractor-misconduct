# Project McNulty

### Proposal

I plan on using The Project On Government Oversight's [Federal Contractor Misconduct Database](https://www.contractormisconduct.org/), which consists of ~2,500 incidents of federal contractors breaking laws or regulations. My goal is to guess the `Disposition Type` dimension, whose 13 classes indicate the resolution of the case (e.g. paid a fine, settled out of court). The most relevant features are the type of misconduct (18 classes), the government agency the contractor worked for (35), and the enforcement agency involved (48). (I could alternatively try to predict whether the contractor paid a fine.)

From those features I think the predictions will be pretty rough, so I'd like to add other features. In particular I've already parsed the disclosures that congressional lobbyists are legally obligated to file. I can match the lobbying firms' clients to some of the offending contractors to get a 'has a lobbyist' feature and probably a couple more. If I have time I'd look into additional data sources about the contractors.

### Contents

* `data/`
  * `contractor_misconduct.csv` - all data from The Project On Government Oversight's [Federal Contractor Misconduct Database](https://www.contractormisconduct.org/)
  * `clean/` - data after cleaned in `clean_misconduct.ipynb`
    * \*`indicators`\* - with indicator dimensions for training
    * the rest - compact, for analysis
* `notebooks/`
  * `clean_misconduct.ipynb` - extract from CSV source and clean
  * `misconduct_add_indicators.ipynb` - add indicators (depends on `clean_misconduct`)
  * `knn.ipynb` - perform cross validation on KNN model (depends on `misconduct_add_indicators`)
  * `extract_disclosures.ipynb` - extract from lobbyist disclosures from XML source (not included)

### Setup
Run, in order:
1. `clean_misconduct.ipynb`
2. `misconduct_add_indicators.ipynb`
3. any model you want to run
