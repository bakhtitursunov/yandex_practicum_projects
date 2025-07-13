🐄 Predicting Milk Yield and Taste for Cow Selection
📌 Project Description
This project was completed as part of a machine learning training program. A farmer from the "Volny Lug" dairy farm wants to expand his herd by purchasing new cows from the supplier "EcoFerma". To minimize risks and ensure high milk quality, he needs two predictive models:

Milk Yield Prediction — to estimate annual milk output per cow;

Milk Taste Prediction — to assess whether the milk will meet the farmer’s taste criteria.

The supplier provided data on their cows, including genetic and feed characteristics. Based on historical data from the farm, the models help select only those cows that are expected to produce at least 6000 kg of milk per year and high-quality milk.

This project demonstrates a full cycle of applied ML: from EDA and feature engineering to regression and classification modeling, with recommendations based on the results.

🗂️ Project Structure
notebook.ipynb — full project in Jupyter Notebook format (with EDA, modeling, and conclusions);

ferma_main.csv — current herd data;

ferma_dad.csv — cow fathers' names;

cow_buy.csv — cow data from the seller.

🧠 Tasks
Perform exploratory data analysis and correlation study;

Build three linear regression models to predict annual milk yield:

Baseline;

With nonlinear feature transformations;

With added feature (father's name);

Build a logistic regression model to predict milk taste;

Use the best models to make predictions for cows available for purchase;

Select cows meeting the required criteria: yield ≥ 6000 kg and good taste.

🔧 Tools & Libraries
Python, pandas, matplotlib, seaborn

scikit-learn (LinearRegression, LogisticRegression, metrics, preprocessing)

scipy (statistical testing)

📈 Key Results
Best linear regression model achieved [R² value] on the test set;

Important nonlinear dependencies were identified and addressed;

The logistic model's recall was prioritized due to the critical nature of selecting only cows with tasty milk;

Final selection: [X cows] matched both quality and productivity criteria.