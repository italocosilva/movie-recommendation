# MovieLens Recommendation System

- This repository contains code and resources for building a movie recommendation system using the MovieLens dataset. The dataset is too large to be included in the repository, but you can generate it using the provided `01_split_data.ipynb` notebook.

## Introduction

- This repository focuses on building a movie recommendation system using the MovieLens dataset. The recommendation models are trained on historical movie ratings, and the system aims to predict user preferences for movies they have not yet seen. Explore the code and resources to understand the implementation details of the recommendation system.

- Feel free to contribute, report issues, or provide feedback to enhance the functionality and performance of the recommendation system.

## Folder Structure

- **notebooks**
  - `01_split_data.ipynb`: Jupyter notebook for splitting and preprocessing the data.
  - `02_nn_model_oot.ipynb`: Jupyter notebook for training the neural network model on out-of-time data.
  - `03_nn_model_oos.ipynb`: Jupyter notebook for training the neural network model on out-of-sample data.
  
- **LICENSE**: The license file specifying the terms under which the code and resources are shared.
- **data**
  - **01_raw**
    - `ratings.csv`: Contains user ratings for movies.
    - `movies.csv`: Details about the movies in the dataset.
    - `genome-tags.csv`: Tags associated with movies for genome data.
    - `links.csv`: Links to external resources related to movies.
    - `genome-scores.csv`: Genome scores for movies.
    - `tags.csv`: Tags assigned to movies by users.
  - **02_model_input**
    - `df_test_oos.parquet.gzip`: Test data for out-of-sample evaluation in Parquet format.
    - `df_train_oos.parquet.gzip`: Training data for out-of-sample evaluation in Parquet format.
    - `df_test.parquet.gzip`: Test data in Parquet format.
    - `df_train.parquet.gzip`: Training data in Parquet format.

## Generating Data

- To generate the dataset, use the `01_split_data.ipynb` notebook provided in the `notebooks` directory. The data files are too large to be included, so running the notebook is necessary.

## Results

- The recommendation system was evaluated on two sets: out-of-time (OOT) and out-of-sample (OOS). The obtained results are as follows:
  - Out-of-Time (OOT) RMSE: 1.1374
  - Out-of-Sample (OOS) RMSE: 0.8039

## Benchmark Comparison

- Comparing the out-of-sample (OOS) results with benchmarks from [Data Science Stack Exchange](https://datascience.stackexchange.com/questions/29740/benchmark-result-for-movielens-dataset):
  - Benchmark for MovieLens 20M using Factorization Machine:
    - MAE: 0.60
    - RMSE: 0.80
  - Benchmark for MovieLens 20M using Autoencoders:
    - RMSE: 0.81

- The results from our recommendation system indicate competitive performance with the benchmarks.
