# Web Recommender Systems 2025: Project

Davide Marchi - lnx547@alumni.ku.dk

This project explores the development of recommender systems using the Amazon Musical Instruments 5-core dataset. It includes data cleaning, exploratory analysis, and the implementation of multiple recommendation techniques, including collaborative filtering, content-based methods, and hybrid approaches that combine both.

---

## Project Structure

The project is organized into the following Jupyter notebooks:

| Notebook                      | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| `Project Week 06.ipynb`       | Cleans and preprocesses the raw dataset, performs exploratory analysis, and exports cleaned datasets. |
| `Project Week 07-11.ipynb`    | Implements a variety of recommender models, including collaborative filtering (TopPop, KNNWithMeans, SVD), content-based filtering using item descriptions, and hybrid strategies that integrate both approaches. |

---

## Execution Instructions

1. **Dataset Preparation**  
   Download the Amazon 5-core Musical Instruments dataset and place `train.tsv` and `test.tsv` inside a `Data/` directory.

2. **Run Notebook 1**  
   Execute `Project Week 06.ipynb`. This notebook processes the raw data and generates:
   - `Data/clean_train.tsv`
   - `Data/clean_test.tsv`

3. **Run Notebook 2**  
   Execute `Project Week 07-11.ipynb`. This notebook uses the cleaned data to train and evaluate the recommendation models.

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