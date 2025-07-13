# 🛴 GoFast Scooter Rental: Statistical Data Analysis

## 📌 Project Overview

As a data analyst for the popular GoFast scooter rental service, you were given data on user behavior across several cities. Your task is to perform exploratory data analysis and hypothesis testing to uncover insights that can help grow the business.

GoFast operates through a mobile app and offers two pricing models:

- **Without subscription**:
  - No monthly fee
  - Ride start fee: 50 RUB
  - Price per minute: 8 RUB

- **With Ultra subscription**:
  - Monthly fee: 199 RUB
  - No start fee
  - Price per minute: 6 RUB

## 📁 Project Contents

- `gofast_analysis.ipynb` — main notebook with code, charts, and conclusions
- `data/users_go.csv` — user data
- `data/rides_go.csv` — ride history
- `data/subscriptions_go.csv` — subscription plan details

## 📊 Datasets Description

### **users_go.csv**

| Column             | Description                           |
|--------------------|----------------------------------------|
| `user_id`          | Unique user ID                         |
| `name`             | User name                              |
| `age`              | Age of the user                        |
| `city`             | City of residence                      |
| `subscription_type`| Type of subscription (`free`, `ultra`) |

### **rides_go.csv**

| Column     | Description                                                           |
|------------|------------------------------------------------------------------------|
| `user_id`  | User ID (matches `users_go.csv`)                                       |
| `distance` | Distance traveled in the ride (in meters)                              |
| `duration` | Duration of the ride (in minutes)                                      |
| `date`     | Date of the ride                                                       |

### **subscriptions_go.csv**

| Column             | Description                          |
|--------------------|--------------------------------------|
| `subscription_type`| Type of subscription                 |
| `minute_price`     | Price per ride minute (in RUB)       |
| `start_ride_price` | Price for ride start (in RUB)        |
| `subscription_fee` | Monthly subscription cost (in RUB)   |

## 🧪 Analysis Plan

### 1. Data Loading
- Read all CSV files using `pandas`
- Explore structure and preview rows

### 2. Data Preprocessing
- Convert date column to datetime
- Extract month from ride date
- Handle missing values and duplicates

### 3. Exploratory Data Analysis (EDA)
- Distribution of users by city
- Ratio of free vs. subscribed users
- Age distribution
- Trip distances and durations

### 4. Merging Datasets
- Merge user, ride, and subscription data
- Split data into two groups: with and without subscription
- Compare ride distance and duration between the two groups

### 5. Revenue Calculation
- For each user and each month:
  - Total ride distance
  - Number of rides
  - Total ride time
  - Monthly revenue (based on pricing model)
  - Round ride duration **up** to the nearest minute

### 6. Hypothesis Testing

#### 📌 Hypothesis 1
> Do users with a subscription spend more time on rides?

Use session duration data to test the difference in ride times.

#### 📌 Hypothesis 2
> Is the average ride distance of subscribed users less than or equal to 3130 meters?

This checks if scooter wear-and-tear stays within optimal limits.

#### 📌 Hypothesis 3
> Is monthly revenue from subscribed users higher than from free users?

Compare monthly revenue per user by subscription type.

#### 📌 Hypothesis 4
> After a server update, did the number of customer support requests significantly decrease?

Determine which statistical test is needed to evaluate this.

### 7. (Optional) Distribution Modeling

#### 🎯 Task 7.1
> A marketing campaign offers free 1-month subscriptions. The goal is for at least **100 users** to renew the subscription.  
> Based on previous data, **10%** of users renew after a free month.  
> How many promo codes should be sent to ensure ~5% chance of **missing** the goal?

- Use binomial distribution
- Visualize and calculate the probability

#### 🎯 Task 7.2
> 40% of users open push notifications.  
> Marketing plans to send **1 million** messages.  
> Estimate the probability that **no more than 399,500** users open the notification.

- Use normal approximation for binomial distribution

## 🛠 Tools & Technologies

- Python
- Pandas
- Seaborn / Matplotlib
- Scipy.stats
- Jupyter Notebook

---
