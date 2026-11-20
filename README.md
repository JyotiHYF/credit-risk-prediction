# Credit Risk Prediction: Clear and Fair

A team project for the ReDI AI course.

## What is this project?

When someone applies for a loan, the bank needs to estimate how likely it is that the person will repay it. We use public data of past loans to build a model that gives each new applicant a risk score, explains the reasons behind it, and checks how fair the results are.

## Our goals

1. Predict whether a loan will be repaid or will default.
2. Use only information a bank would know on the day of the application, so the results are realistic (no data leakage).
3. Compare a simple model with stronger ones and measure them properly, not just with accuracy.
4. Explain each prediction and check the results across groups, being open about the limits.
5. Show the result in a small web page.

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

```
credit-risk-project/
  data/          (not on GitHub, download from Kaggle)
  notebooks/     our notebooks
  src/           reusable scripts
  api/           the web service for the demo
  README.md
```

## How to run

```bash
git clone https://github.com/YOUR-USERNAME/credit-risk-prediction.git
cd credit-risk-prediction
python3 -m venv .venv
source .venv/bin/activate
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

Then download the data (see above) and open the notebooks in order.

## How we work together

- Nobody pushes straight to `main`. We use a branch and a pull request for every change.
- We always pull before starting work.
- One owner per file.
- Short check-ins twice a week.

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
