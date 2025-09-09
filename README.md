# Quantum One test task

## Overview

This project tackles a **socially impactful machine learning challenge** — predicting financial stress levels (low, moderate, high) among gig economy workers using behavioral, occupational, and financial data. The goal is to build an accurate multiclass classification model that can help fintech startups, mental health platforms, and labor unions identify individuals at risk for financial stress and design timely supportive interventions.

The model leverages the powerful [CatBoost](https://catboost.ai/) gradient boosting framework combined with hyperparameter tuning via [Optuna](https://optuna.org/) and robust cross-validation strategies.

***

## Dataset

- **train.csv** — labeled training dataset including worker behaviors, income, credit details, spending patterns, and target financial stress levels.
- **test.csv** — unlabeled dataset for which predictions are generated.
- **sample_submission.csv** — submission format example.

The dataset covers detailed features such as:

- Worker demographics (age, job sector)
- Financial activity (income, liabilities, credit cards, loans)
- Digital behavior patterns and spending habits
- Credit history indicators (missed payments, credit checks)

***

## Key Features of This Solution

- **Data Preprocessing**: Custom parsing and transforming complex features (e.g., credit age in years and months converted into numeric months).
- **Robust Modelling**: Utilizing CatBoost with GPU acceleration for efficient training of multiclass classification.
- **Hyperparameter Optimization**: Leveraging Optuna for automated selection of optimal model parameters.
- **Cross-Validation**: GroupKFold strategy by `worker_id` to prevent data leakage and more realistic evaluation.
- **Early Stopping**: Preventing overfitting with early stopping rounds during training.
- **Submission Generation**: Predicting stress levels aligned with the competition’s submission format.

***

## How to Run

1. Clone the repository
```bash
git clone https://github.com/TyurinIvan/quantum-one-test-task.git
cd quantum-one-test-task
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

or install core packages directly:

```bash
pip install catboost[gpu] optuna pandas scikit-learn
```

3. Place `train.csv`, `test.csv`, and `sample_submission.csv` in the working directory.
4. Run the notebook or Python script to train and generate predictions:
```bash
jupyter notebook predict_financial_stress.ipynb
```

The submission file `submission.csv` will be generated automatically.

***

## Results \& Metrics

- Best achieved accuracy on cross-validation: **~68% - 68.5%**
- Model interpretability and feature importance confirm key financial health indicators drive predictions

***

## Future Improvements

- Incorporating time-series modeling over survey months to capture temporal trends
- Using neural nets or ensemble models blending multiple algorithms
- Advanced feature extraction from digital behavioral signals
- More granular stress level categorization or regression modeling for continuous stress scores

***

## Acknowledgments

- Thanks to [CatBoost Team](https://catboost.ai/) for the excellent gradient boosting implementation
- [Optuna](https://optuna.org/) for efficient hyperparameter tuning framework
- Quantum-One for providing the stimulating test assignment dataset

***

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
<span style="display:none">[^1][^10][^2][^3][^4][^5][^6][^7][^8][^9]</span>

<div style="text-align: center">⁂</div>

[^1]: https://www.youtube.com/watch?v=syrGPPekLHQ

[^2]: https://pai-bx.com/wiki/more/2595-the-complete-guide-to-markdown-design-readme-md/

[^3]: https://skillbox.ru/media/code/yazyk-razmetki-markdown-shpargalka-po-sintaksisu-s-primerami/

[^4]: https://docs.github.com/ru/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

[^5]: https://github.com/artyomboyko/Markdown

[^6]: https://doka.guide/tools/markdown/

[^7]: https://gist.github.com/Jekins/2bf2d0638163f1294637

[^8]: https://gist.github.com/fomvasss/8dd8cd7f88c67a4e3727f9d39224a84c

[^9]: https://ru.hexlet.io/blog/posts/chto-takoe-markdown-i-zachem-on-nuzhen

[^10]: https://kokoc.com/blog/markdown/

