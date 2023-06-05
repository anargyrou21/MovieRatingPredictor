# Project Title

## 1. Dataset:
* [movie_data_preparation.ipynb](./movie_data_preparation.ipynb)

## 2. Run code

Clone the project

```bash
  git clone https://link-to-project
```

Go to the project directory

```bash
  cd project_folder
```

Install libraries

```bash
  pip install -r requirements.txt
```

Prepare dataset

```bash
  jupyter notebook movie_data_preparation.ipynb
```

Run notebook EDA and Model on dataset

```bash
  jupyter notebook movie_data.ipynb
```

## 3. Roadmap
- Prepare api_key from [The movie db api](https://api.themoviedb.org).
- Collect data from [The movie db api](https://api.themoviedb.org).
- Movie data will be preprocessed, EDA before feed to model regression.
- After training model, will calculate score to compare them.

## 4. Feature Processed
| Parameter       | Type     |
|:----------------|:---------|
| `imdb_id`      | `Object` |
| `title`      | `Object` |
| `overview`   | `Object` |
| `release_date`      | `Object` |
| `runtime`   | `Int`    |
| `status` | `Object` |
| `tagline`    | `Object` |
| `adult`    | `Bool`   |
| `vote_average`  | `Float`  |
| `vote_count`  | `Int`    |
| `genres`   | `Object` |
| `production_companies`   | `Object` |
| `directors`   | `Object` |
| `actors`   | `Object` |
| `rating_rounded`      | `Int`    |


## 5. Models
- [SVM](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVR.html)

    Epsilon-Support Vector Regression. SVMs excel in handling high-dimensional data, effectively mitigating overfitting, and accommodating non-linear patterns using kernel functions.
- [Random Forest](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)

    A random forest is a meta estimator that fits a number of classifying decision trees on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting.
- [ANN]()

  An artificial neural network (ANN) is a computational model inspired by the structure and function of the human brain, consisting of interconnected nodes (neurons) that process and transmit information. It is widely used in machine learning and deep learning tasks to solve complex problems by learning from large amounts of data..

## 6. Evaluate
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)

## 7. Deployment
For deploy, we can use cloud service: **AWS**, **Azure**, **GCP**,...

## 8. License
[MIT](https://choosealicense.com/licenses/mit/)

## 9. Authors
- [Andreas]
