# Scoring Movies Based on Movie Data from The Movie Database

## 0. Overview
  This project aims to develop a scoring system for movies based on various movie attributes using data obtained from the TMDb API (https://api.themoviedb.org). The goal is to evaluate different machine learning models and determine the most effective one for predicting movie scores. Three models were employed for this task: Random Forest Regression, Support Vector Machine (SVM) Regression, and Artificial Neural Network (ANN). Through experimentation and evaluation, it was found that the SVM Regression model performed the best among the three models.

- [Scoring Movies Based on Movie Data from The Movie Database](#project-title)
  - [0. Overview](#0-overview)
  - [1. Dataset](#1-dataset)
  - [2. Run code](#2-run-code)
  - [3. Roadmap](#3-roadmap)
  - [4. Feature Processed](#4-feature-processed)
  - [5. Models](#5-models)
  - [6. Evaluate](#6-evaluate)
  - [7. Deployment](#7-deployment)
  - [8. License](#8-license)
  - [9. Authors](#9-authors)

## 1. Dataset
The project relies on the TMDb API to retrieve movie data, including information such as title, release year, genre, runtime, budget, and popularity. This data serves as the feature set used for training and evaluating the machine learning models. The API provides a vast collection of movies, ensuring a diverse dataset for model training.

| Parameter       | Type     | Sample Value                                         |
|:----------------|:---------|:-----------------------------------------------------|
| `imdb_id`      | `Object` | `tt10366206`                                         |
| `title`      | `Object` | `John Wick: Chapter 4`                               |
| `overview`   | `Object` | `With the price on his head ever increasing, Jo...`  |
| `release_date`      | `Object` | `2023-03-22	`                                        |
| `runtime`   | `Int`    | `170`                                                |
| `status` | `Object` | `Released`                                           |
| `tagline`    | `Object` | `No way back, one way out.`                          |
| `adult`    | `Bool`   | `False`                                              |
| `vote_average`  | `Float`  | `7.979`                                              |
| `vote_count`  | `Int`    | `2337`                                               |
| `genres`   | `Object` | `['Action', 'Thriller', 'Crime']`                    |
| `production_companies`   | `Object` | `['Thunder Road', '87Eleven', 'Summit Entertain...`  |
| `directors`   | `Object` | `['Chad Stahelski']`                                 |
| `actors`   | `Object` | `['Keanu Reeves', 'Donnie Yen', 'Bill Skarsgård...	` |
| `rating_rounded`      | `Int`    | `8`                                                  |

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
- Prepare `api_key` from [The movie db api](https://api.themoviedb.org).
- Collect data from [The movie db api](https://api.themoviedb.org).
- Movie data will be preprocessed, EDA before feed to model regression.
- After training model, will calculate score to compare them.

## 4. Feature Processed
To prepare the movie data for the machine learning models, feature engineering techniques were applied. This involved transforming and encoding categorical variables, handling missing data, and scaling numerical features to ensure compatibility with the models. The engineered features were then used to train and evaluate the models.

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

## 7. Test
- Input data:
```python
title = 'Fast X'
overview = "Over many missions and against impossible odds, Dom Toretto and his family have outsmarted, out-nerved and outdriven every foe in their path. Now, they confront the most lethal opponent they've ever faced: A terrifying threat emerging from the shadows of the past who's fueled by blood revenge, and who is determined to shatter this family and destroy everything—and everyone—that Dom loves, forever."
tagline = 'The end of the road begins'
genres = 'Action Crime Thriller'
production_companies = 'Universal Pictures Original Film One Race Perfect Storm Entertainment'
directors = 'Louis Leterrier'
actors = 'Vin Diesel Michelle Rodriguez Tyrese Gibson Ludacris John Cena Nathalie Emmanuel Jordana Brewster Sung Kang Jason Momoa Scott Eastwood'
```
- Model return: `Rating Score: 6.626475234867884`



## 8. Deployment
For deploy, we can use cloud service: **AWS**, **Azure**, **GCP**,...

## 9. License
[MIT](https://choosealicense.com/licenses/mit/)


## Support
For support, andreasargyrou21@gmail.com
