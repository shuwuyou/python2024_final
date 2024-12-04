# python2024_final
Here's a suggested README file for your project. It includes details about the objective, methodology, and structure based on typical data cleaning and modeling workflows.

---

# Movie Ratings Prediction Project

## **Project Overview**
This project focuses on predicting movie critic ratings (`critic_rating`) using various features derived from a dataset of movies. The goal is to build a robust model that can predict critic ratings before any audience or critic reviews are posted. The project involves data cleaning, feature engineering, and model development.

---

## **Workflow**

1. **Data Cleaning**  
   - Removed missing values (`NaN`) in both feature and target variables to ensure clean and reliable data.
   - Combined training and target datasets for consistent dropping of rows with missing data.
   - Dropped features that would not be available pre-release (e.g., `critic_rating`, `critic_count`, `audience_rating`, `audience_count`, `on_streaming_date`).

2. **Feature Engineering**  
   - Created meaningful new features, such as:
     - `kid_friendly`: Binary feature indicating whether a movie is G or PG-rated.
     - `director_popularity`: Binary feature for whether the director is among the top 10 based on movie counts across training and test data.
     - `winter_or_not`: Binary feature indicating if the movie's release season is winter.
     - Interaction terms between genres and other features for better predictions.
   - Explored feature transformations like grouping rare genres and normalizing continuous variables.

3. **Model Development and Exploration**  
   - Developed multiple linear regression models using `statsmodels` and `scikit-learn`.
   - Evaluated models using metrics like R², MAE, and RMSE.
   - Explored advanced modeling techniques such as Ridge/Lasso regularization and non-linear models like Random Forests and Gradient Boosting.

4. **Visualization and Insights**  
   - Analyzed patterns in the data using scatter plots, histograms, and pair plots.
   - Identified key features (e.g., `runtime_in_minutes`, `director_popularity`) that significantly impact critic ratings.

---

## **Key Findings**

1. **Data Insights**:
   - Audience and critic ratings are positively correlated, but there are notable exceptions.
   - Most movies have runtimes between 75 and 175 minutes, and movies released after 2000 dominate the dataset.

2. **Model Insights**:
    For required 3 models:
   - The third model performed the best with an R² of 0.13.
   - Features like `runtime_in_minutes`, `kid_friendly`, and genres play a significant role in predicting critic ratings.
   - Including genre variables improves predictive power, as they align with how critics evaluate movies.
    For my personal 3 models:
   - The sixth model performed the best with an R² of 0.187.
   - Features like `runtime_in_minutes`, `kid_friendly`, `director_popularity`, `rated` and genres play a significant role in predicting critic ratings.


3. **Improvement Suggestions**:
   - Add more data from APIs like TMDB or OMDB to incorporate additional features (e.g., budget, box office revenue).
   - Perform more advanced feature engineering, such as creating interaction terms or grouping rare categories.
   - Explore advanced models like Random Forests and Gradient Boosting for better performance.

---

## **How to Use This Repository**

1. **Prerequisites**:
   - Python 3.x
   - Libraries: `pandas`, `numpy`, `matplotlib`, `statsmodels`, `scikit-learn`

2. **Files**:
   - `final.ipynb`: Jupyter notebook containing data cleaning, feature engineering, and model development.

3. **Steps to Run**:
   - Open the notebook in a Jupyter environment.
   - Follow the sections to clean the data, engineer features, and train models.
   - Modify or expand the features and models as needed.

4. **Future Work**:
   - Implement advanced models like XGBoost.
   - Incorporate additional datasets for richer feature sets.
   - Use hyperparameter tuning to optimize model performance.

---

## **Contact**
For any questions or suggestions, feel free to reach out.

Let me know if you’d like any modifications to this README or if you need additional sections!