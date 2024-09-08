# Discovering the Universe: Classifying Exoplanets with Machine Learning

In this project, I leveraged data from NASA’s Kepler Space Telescope to classify exoplanets as confirmed, candidates, or false positives. Key features such as Kepler magnitude, orbital period, and planet size were analyzed through extensive Exploratory Data Analysis (EDA) to gain insights into the universe.

Process:

Exploratory Data Analysis (EDA):

Analyzed various features like planet size, orbital period, and stellar properties to understand patterns in the data.
Visualized key relationships between the features and target labels.


Preprocessing:

Handled missing values by imputation and removed irrelevant or low-importance features.


Model Building and Selection:

I tried various machine learning models, including Random Forest and XGBoost, but after careful comparison, LightGBM emerged as the best-performing model due to its efficiency, speed, and handling of complex, structured data. LightGBM outperformed other models in accuracy and training speed, making it ideal for this task.
After tuning the models, I achieved an accuracy of 91% with LightGBM. The model provides a reliable way to classify exoplanets, offering potential benefits for future astronomical discoveries by distinguishing real planets from false positives.


Model Evaluation:

In this project, the model’s performance was evaluated using key metrics such as accuracy, precision, recall, and the F1-score. These metrics are crucial, especially for a classification problem like exoplanet detection, where false positives and false negatives can have significant implications.

