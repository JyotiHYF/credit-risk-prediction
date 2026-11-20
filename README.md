# Credit Risk Prediction: Clear and Fair

A team project for the ReDI AI course.

## What is this project?

When someone applies for a loan, a bank needs to assess the risk of whether the borrower will repay it. In this project, we use historical LendingClub loan data to develop a machine learning system that predicts the likelihood of loan default.

Our goal is to build an end-to-end credit risk prediction solution that:

- Predicts loan default risk using machine learning.
- Explains model predictions using SHAP.
- Evaluates model performance using appropriate metrics.
- Examines fairness across relevant groups.
- Presents predictions through a simple web application.

This is an educational project and is not intended for real-world lending decisions.

## Our Goals

1. **Prediction:** Predict whether a loan will be fully repaid or charged off.
2. **Data quality:** Use information available at loan application time and prevent data leakage.
3. **Model comparison:** Compare Logistic Regression, Random Forest and XGBoost.
4. **Evaluation:** Measure performance using precision, recall, ROC-AUC, PR-AUC and confusion matrices.
5. **Explainability:** Use SHAP to understand the factors influencing predictions.
6. **Fairness:** Evaluate model outcomes across relevant groups and discuss potential bias and limitations.
7. **Deployment:** Build a simple web application connected to a FastAPI prediction endpoint.

## Data

We use the public LendingClub loan dataset from Kaggle: https://www.kaggle.com/datasets/wordsforthewise/lending-club

The data is **not stored in this repository** because the files are very large. To run the project:

1. Download the dataset from Kaggle.
2. Put the `accepted` CSV file in `data/archive/`.
3. We work with a sample of the first 100,000 rows.

Note: this is US data from past years. It is used here for learning, and the same method would be trained on a bank's own data in real life.

## Team and roles

| Member  | Role                                                    | Main files                                       |
| ------- | ------------------------------------------------------- | ------------------------------------------------ |
| member1 | Data: loading, cleaning, safe columns, train/test split | `notebooks/01_data.ipynb`, `src/prepare_data.py` |
| member2 | Models and evaluation                                   | `notebooks/02_models.ipynb`                      |
| member3 | Explanations, fairness check and web page               | `notebooks/03_explain.ipynb`, `api/`             |

## Project structure

credit-risk-project/
│
├── data/
│ ├── archive/
│ └── processed/
│
├── notebooks/
│ ├── 01_data.ipynb
│ ├── 02_models.ipynb
│ └── 03_explain.ipynb
│
├── src/
│ └── prepare_data.py
│
├── models/
│
├── api/
│ └── main.py
│
├── webpage/
│
├── requirements.txt
├── .gitignore
└── README.md

## How to run

```bash
git clone https://github.com/YOUR-USERNAME/credit-risk-prediction.git
cd credit-risk-prediction
python3 -m venv .venv
source .venv/bin/activate
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

Then download the data (see above) and open the notebooks in order.

## How We Work Together

### Branching strategy

- `main`: Stable and tested version of the project.
- `develop`: Integration branch for team development.
- `feature/*`: Individual branches for new features and tasks.

### Team rules

1. Nobody pushes directly to `main`.
2. Every change must go through a Pull Request.
3. Always pull the latest changes before starting work.
4. Each file has one primary owner to avoid conflicts.
5. Review and test changes before merging.

### Weekly collaboration

- Two 15-minute team check-ins each week.
- Each member shares completed work, next steps and blockers.
- Each member explains their work to the team at least once a week.
- Team members help each other understand the complete project.

## Status

- [x] Project setup
- [ ] Data preparation
- [ ] Models and evaluation
- [ ] Explanations and fairness
- [ ] Web page
- [ ] Final presentation

## Limitations

- US data from past years, not Danish data.
- We use a sample of the full dataset.
- The model supports a decision. A human should make the final decision.
