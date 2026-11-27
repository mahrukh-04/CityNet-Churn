# CityNet churn baseline

## User story
As the retention manager, I want a weekly list of the 100 customers most likely to cancel next month, so my team can call them first.

## How to run
```bash
pip install -r requirements.txt
python src/lab7_save.py                 # train and save the pipeline
python src/predict.py data/new_customers.csv  # writes reports/predictions.csv
```

## Results (validation, then test once)

| Metric | Baseline | Our model |
|---|---:|---:|
| PR-AUC | 0.179 (5-fold CV) | 0.396 (validation); 0.361 (test) |
| Churners in top 100 | About 18 (random selection) | 49 (validation) |

## Intended use
Prioritizing the 100 customers with the highest predicted churn risk for retention team outreach.

## Not for
Making automatic decisions about customers, or treating predictions as certain outcomes.

## Assumptions
New customer data has the same required input features and format as the training data. The churn patterns in new data are reasonably similar to those in the training dataset.

## Risks and limitations
The dataset is imbalanced, with only 17.9% churners. The model can miss actual churners and may perform differently across regions. The data is made-up course data, so results may not represent real customers.
