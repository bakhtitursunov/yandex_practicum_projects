# 🏠 Real Estate Price Analysis in St. Petersburg

## 📌 Project Overview

This project explores real estate data from the Yandex Real Estate service — a dataset of historical apartment listings in St. Petersburg and surrounding areas over several years. The goal is to identify the key factors that influence real estate prices and build a foundation for an automated system to detect pricing anomalies and potential fraudulent behavior.

The dataset includes two types of information:
- **User-entered data** (e.g., price, number of rooms)
- **Geo-based data** retrieved automatically (e.g., distance to the center, number of parks nearby)

## 📁 Project Contents

- `real_estate_analysis.ipynb` — main notebook with data cleaning, exploration, and insights
- `data/real_estate_data.csv` — dataset from Yandex Real Estate

## 📊 Data Description

| Column                  | Description                                         |
|-------------------------|-----------------------------------------------------|
| `airports_nearest`      | Distance to nearest airport (m)                     |
| `balcony`               | Number of balconies                                 |
| `ceiling_height`        | Ceiling height (m)                                  |
| `cityCenters_nearest`   | Distance to city center (m)                         |
| `days_exposition`       | Days the listing was active                         |
| `first_day_exposition`  | Date of first publication                           |
| `floor`                 | Floor number                                        |
| `floors_total`          | Total floors in the building                        |
| `is_apartment`          | Whether the property is an apartment (True/False)   |
| `kitchen_area`          | Kitchen area (m²)                                   |
| `last_price`            | Listing price                                       |
| `living_area`           | Living area (m²)                                    |
| `locality_name`         | Name of the locality                                |
| `open_plan`             | Open floor plan (True/False)                        |
| `parks_around3000`      | Number of parks within 3 km                         |
| `parks_nearest`         | Distance to nearest park (m)                        |
| `ponds_around3000`      | Number of ponds within 3 km                         |
| `ponds_nearest`         | Distance to nearest pond (m)                        |
| `rooms`                 | Number of rooms                                     |
| `studio`                | Studio apartment (True/False)                       |
| `total_area`            | Total area (m²)                                     |
| `total_images`          | Number of images in the listing                     |

## 🔍 Key Steps in the Analysis

### 1. Data Exploration
- Load and inspect the dataset
- Generate histograms for numerical features
- Identify and describe data quality issues

### 2. Data Preprocessing
- Handle missing values where appropriate (e.g., replace missing `balcony` values with 0)
- Convert data types for efficiency and accuracy
- Clean inconsistent locality names
- Comment on possible reasons for missing values

### 3. Feature Engineering
- Add calculated columns:
  - Price per square meter
  - Day of the week, month, and year of publication
  - Floor type (first, last, other)
  - Distance to city center (in km)

### 4. Exploratory Data Analysis
- Visualize distributions of key features:
  - Total area, living area, kitchen area, ceiling height
  - Number of rooms, floor type, building height
  - Distance to city center and nearest park
- Analyze how long apartments are listed (`days_exposition`)
  - Histogram, mean, median
  - Define what counts as fast and slow sales
- Identify factors most affecting the final price:
  - Total/living/kitchen area, number of rooms, floor level, and listing date
- Use pivot tables and plots to explore dependencies

### 5. Geographic Analysis
- Determine average price per square meter in the 10 most active localities
- Highlight the most and least expensive areas
- Analyze how distance from city center affects apartment price
  - Focus on listings within St. Petersburg
  - Group by distance in kilometers

## 🧠 Conclusion

A comprehensive analysis was conducted on real estate data to determine which features most affect apartment prices. This insight lays the groundwork for building an automated pricing and fraud detection system for real estate listings.

## 🛠 Tools & Technologies

- Python
- Pandas
- Matplotlib & Seaborn
- Jupyter Notebook

---
