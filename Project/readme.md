# Web Recommender Systems 2025: Project

Davide Marchi - lnx547@alumni.ku.dk

This project implements a recommender system using the Amazon Musical Instruments 5-core dataset. It includes data preprocessing, exploratory analysis, collaborative filtering models, and evaluation based on both accuracy and recommendation quality.

---

## Project Structure

The project consists of two Jupyter notebooks:

| Notebook                                | Description                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------|
| `week06_data_cleaning_and_eda.ipynb`    | Cleans and preprocesses the raw dataset, performs exploratory analysis, and exports cleaned datasets. |
| `week07_08_cf_models_and_evaluation.ipynb` | Implements and evaluates collaborative filtering recommenders including TopPop, KNNWithMeans, and SVD using the Surprise library. |

---

## Execution Instructions

1. **Dataset Preparation**  
   Download the Amazon 5-core Musical Instruments dataset and place `train.tsv` and `test.tsv` inside a `Data/` directory.

2. **Run Notebook 1**  
   Execute `week06_data_cleaning_and_eda.ipynb`. This notebook processes the raw data and generates:
   - `Data/clean_train.tsv`
   - `Data/clean_test.tsv`

3. **Run Notebook 2**  
   Execute `week07_08_cf_models_and_evaluation.ipynb`. This notebook uses the cleaned data to train and evaluate the recommendation models.

---

## Environment and Dependencies

The project was developed using Python 3.10.16. The following packages are required:

| Package          | Version |
|------------------|---------|
| python           | 3.10.16 |
| pandas           | 2.2.3   |
| numpy            | 1.26.4  |
| matplotlib       | 3.10.0  |
| scikit-learn     | 1.6.1   |
| scikit-surprise  | 1.1.4   |
| nltk             | 3.9.1   |
| gensim           | 4.3.3   |
| seaborn          | 0.13.2  |

To install the dependencies:

```bash
pip install pandas==2.2.3 numpy==1.26.4 matplotlib==3.10.0 \
            scikit-learn==1.6.1 scikit-surprise==1.1.4 nltk==3.9.1 \
            gensim==4.3.3 seaborn==0.13.2
```

---

## Evaluation Metrics

The following metrics are used to assess model performance:

- Root Mean Squared Error (RMSE)
- Precision@10
- Mean Average Precision (MAP@10)
- Mean Reciprocal Rank (MRR@10)
- Hit Rate
- Coverage

---

## Notes

- All users in the test set are ensured to exist in the training set.
- Data deduplication and preprocessing steps are documented in Notebook 1.
- The evaluation highlights trade-offs between different recommender models:
  - SVD provides better RMSE.
  - KNNWithMeans offers better item diversity and coverage.
  - TopPop performs strongly in ranking metrics due to its bias toward popular items.
