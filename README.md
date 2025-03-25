# IMDb Data Analysis

## Project Overview
This project analyzes the IMDb Top 1000 movies dataset, performing data preprocessing, exploratory data analysis (EDA), regression modeling, and visualization to extract insights about the most popular films.

## Dataset
The dataset used in this analysis is `imdb_top_1000.csv`, which contains various attributes of top-rated movies, such as:

* **Poster_Link** - Link to the poster used by IMDB
* **Series_Title** - Movie title
* **Released_Year** - Year of release
* **Certificate** - Age rating certification
* **Runtime** - Total runtime of the movie
* **Genre** - Movie genre
* **IMDB_Rating** - IMDB rating of the movie
* **Overview** - Story summary
* **Meta_score** - Score earned by the movie
* **Director** - Name of the director
* **Star1, Star2, Star3, Star4** - Names of the main actors
* **No_of_votes** - Total number of votes
* **Gross** - Revenue earned by the movie

## Requirements
To run this project, install the following dependencies:
```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

## Steps in Analysis
### 1. Data Loading and Preprocessing
- The dataset is read using Pandas.
- Column names are converted to lowercase for consistency.
- Basic data integrity checks are performed.

### 2. Exploratory Data Analysis (EDA)
- Checking for missing values and handling them appropriately.
- Visualizing distributions of key features like IMDb ratings, runtime, and genre distribution.
- Analyzing correlations between features.

### 3. Regression Modeling
- Implemented **Lasso Regression** and **XGBoost Regression** to predict IMDb ratings based on various features.
- Used `train_test_split` to split the dataset into training and testing sets.
- Tuned hyperparameters using `GridSearchCV` for optimal performance.
- Evaluated models using:
  - **R² Score**: Measures how well the model explains variance in the target variable.
  - **Mean Squared Error (MSE)**: Quantifies prediction error.

### 4. Visualization
- Bar charts, histograms, and scatter plots are used to explore patterns.
- Heatmaps are generated to examine relationships between numerical features.

## Key Results
- The dataset contains movies from various decades, with a concentration of highly rated films in the 1990s and 2000s.
- The most frequent genres include Drama, Action, and Comedy.
- Directors such as Christopher Nolan and Steven Spielberg appear frequently in the top-rated films.
- Higher IMDb ratings tend to correlate with higher gross revenue, but some exceptions exist.
- **Lasso Regression** provided a simple, interpretable model but underperformed in comparison to XGBoost.
- **XGBoost Regression** outperformed Lasso, achieving a higher R² score and lower prediction error, making it a better choice for IMDb rating prediction.

## How to Run
Run the Jupyter Notebook step by step to replicate the analysis. Ensure the dataset is available in the working directory before execution.

## Conclusion
This analysis provides insights into what makes a movie highly rated on IMDb, including trends in ratings, popular genres, successful directors, and predictive modeling of IMDb scores.

## License
This project is for educational purposes only. The dataset belongs to its respective owners.

