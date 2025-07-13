# 🎮 Video Game Sales Analysis for Global Market

## 📌 Project Overview

This project focuses on analyzing historical data from the global video game market to identify key factors that influence a game's commercial success. Using sales data, user and critic reviews, platform and genre information, the goal is to uncover actionable insights to support product planning and marketing strategy.

The analysis includes exploring sales trends across platforms, understanding genre profitability, evaluating regional user preferences, and testing statistical hypotheses. Special attention is given to preparing a data-driven forecast for upcoming releases, using the most relevant and recent data available.

This will help the company focus on potentially popular products and plan effective advertising campaigns.

> ⚠️ The dataset includes data up to the end of **2016**. We assume the current date is **December 2016**, and the goal is to prepare a forecast for **2017**.

The dataset contains an **ESRB** rating field — the **Entertainment Software Rating Board**, which assigns age ratings to games, such as "Everyone", "Teen", or "Mature".

## 📁 Project Structure

- `games_analysis.ipynb` — the main notebook with full analysis and conclusions
- `data/games.csv` — dataset with global game sales and reviews

## 📊 Dataset Description

| Column         | Description                                                    |
|----------------|----------------------------------------------------------------|
| `Name`         | Name of the game                                               |
| `Platform`     | Platform (e.g., PS4, Xbox One, PC)                             |
| `Year_of_Release` | Year of release                                             |
| `Genre`        | Game genre                                                     |
| `NA_sales`     | North America sales (in millions of units)                     |
| `EU_sales`     | Europe sales (in millions of units)                            |
| `JP_sales`     | Japan sales (in millions of units)                             |
| `Other_sales`  | Other regions sales (in millions of units)                     |
| `Critic_Score` | Critic rating (out of 100)                                     |
| `User_Score`   | User rating (out of 10)                                        |
| `Rating`       | ESRB rating (e.g., E, T, M)                                     |

> Note: Data for 2016 may be incomplete.

---

## 🧪 Analysis Workflow

### 1. Data Loading & Overview
- Load the dataset from `games.csv`
- Explore basic information and column types

### 2. Data Preprocessing
- Standardize column names to lowercase
- Convert data to appropriate types and handle missing values
  - Explain how and why missing data is handled
  - Handle `'tbd'` values in the user score column
- Create a new column for **total global sales**

### 3. Exploratory Data Analysis
- Analyze the number of game releases per year
- Examine how platform sales have changed over time
- Identify top-performing platforms and their lifecycle duration
- Focus on a **relevant period** to build a 2017 forecast
- Investigate:
  - Top platforms
  - Sales distributions (boxplots)
  - Impact of user and critic scores (scatter plots, correlations)
  - Genre profitability and popularity

### 4. Regional User Profile Analysis
For each region — **North America (NA)**, **Europe (EU)**, and **Japan (JP)**:
- Identify top-5 platforms
- Identify top-5 genres
- Evaluate the impact of ESRB ratings on regional sales

### 5. Hypothesis Testing

#### Hypothesis 1:
> Average user scores for **Xbox One** and **PC** games are equal.

#### Hypothesis 2:
> Average user scores for **Action** and **Sports** games are different.

- Define null and alternative hypotheses
- Choose appropriate statistical test (e.g., t-test)
- Set a significance level (alpha) and interpret the results

### 6. Summary and Conclusions
- Summarize key findings and business recommendations
- Highlight most promising platforms and genres
- Provide insights for the 2017 marketing strategy

---

## 🛠 Tools & Technologies

- Python
- Pandas
- Matplotlib / Seaborn
- Scipy.stats
- Jupyter Notebook

---
