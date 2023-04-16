# Real-Time-Sales-Prediction-Model
Data Collection:
We started with a dataset that contains information about sales of paperback and hardback books on different dates, from '01-04-2000' to '30-04-2000'. The dataset includes columns for 'Date', 'Paperback' sales, and 'Hardback' sales.

Data Preprocessing:
We performed several data preprocessing steps to prepare the data for training a linear regression model:

Date Extraction: We extracted the day of the week, month, and year from the 'Date' column using the 'pd.to_datetime' function from the pandas library. This allowed us to convert the 'Date' column into three separate columns for day of the week, month, and year, which can be used as input features for the model.

Feature Engineering: We created additional features by combining the 'Paperback' and 'Hardback' sales columns. We added these two columns to create a new column 'TotalSales' which represents the sum of 'Paperback' and 'Hardback' sales. This new column serves as our target variable (y) for training the linear regression model.

Feature Selection:
We selected five input features for our model: 'DayOfWeek', 'Month', 'Year', 'Paperback', and 'Hardback'. These features were chosen based on their potential impact on book sales. 'DayOfWeek', 'Month', and 'Year' capture the temporal information, while 'Paperback' and 'Hardback' represent the individual sales of each type of book.

Model Training:
We used the 'LinearRegression' class from the sklearn.linear_model module to create a linear regression model. We assigned the input features (X) and target variable (y) to the respective variables. Then, we called the 'fit' method on the model object to train the model using the input features and target variable.

Model Evaluation:
We predicted the total sales (y_pred) using the trained linear regression model on the same dataset (X) used for training. We then calculated the R-squared score using the 'r2_score' function from the sklearn.metrics module. The R-squared score is a measure of how well the model fits the data, with a higher value indicating a better fit. We printed the R-squared score and the coefficients of the model as evaluation metrics.

Model Interpretation:
We interpreted the coefficients of the model as the impact of each input feature on the target variable. The coefficients represent the change in the target variable for a one-unit change in the corresponding input feature, while keeping other features constant. The intercept represents the estimated target variable when all input features are zero.

Overall, we performed feature engineering, data preprocessing, model training, and evaluation steps to create a linear regression model that predicts total book sales based on various input features. The R-squared score and coefficients of the model provide insights into the model's performance and feature importance, respectively.
