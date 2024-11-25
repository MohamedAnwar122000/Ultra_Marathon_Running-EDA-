# Ultra-Marathon Analysis Project

## Project Purpose
The goal of this project is to analyze ultra-marathon race data to uncover trends, insights, and performance metrics. The analysis aims to answer key questions about athlete performance, race distances, seasonality, and demographic factors such as age and gender. This project provides actionable insights for ultra-marathon athletes, event organizers, and enthusiasts to improve performance and planning.

---

## About the Dataset
The dataset used in this project is titled **"The Big Dataset of Ultra-Marathon Running"**, sourced from [Kaggle](https://www.kaggle.com/datasets/aiaiaidavid/the-big-dataset-of-ultra-marathon-running). It contains over **7.4 million race records** from **1.6 million unique athletes**, spanning a period from **1798 to 2022**.

### Key Features:

#### **Event Details**
- **Event name**: Name and location of the event.
- **Event distance/length**: Race distances (e.g., 50km, 100mi) or time-based races (e.g., 6h, 24h).
- **Year of event** and **Event date**: Temporal information for each race.
- **Event number of finishers**: Total number of finishers for each event.

#### **Athlete Details**
- **Athlete performance**: Time taken by athletes to complete the race.
- **Athlete club**: Club or organization associated with the athlete.
- **Athlete country**: Country represented by the athlete.
- **Athlete gender**: Gender of the athlete (Male, Female, or X).
- **Athlete age**: Categorized age group (e.g., M23, W35).
- **Athlete average speed**: Speed (in km/h) calculated for each race.

#### **Unique Identifiers**
- **Athlete ID**: Unique identifier for each athlete to track performances across multiple races.

This dataset is ideal for exploring long-term trends in ultra-marathon running, comparing athlete performance, and analyzing race characteristics.

---

## Approach Used in This Project

### **Step 1: Data Import and Initial Inspection**
- Load the dataset into a Pandas DataFrame.
- Inspect the structure, data types, and missing values in the dataset.

### **Step 2: Data Cleaning**
- **Handle missing values**:
  - Drop rows with missing values in key columns like `athlete_age` and `athlete_average_speed`.
- **Remove invalid data entries**:
  - Exclude rows where `athlete_gender` is "X".
- **Normalize and transform data**:
  - Extract race months from the `Event date`.
  - Categorize races into seasons (e.g., Winter, Spring, Summer, Fall).

### **Step 3: Data Transformation**
- **Create derived columns**:
  - `race_season`: Assign seasons based on race months.
  - `athlete_age_group`: Categorize athletes into broader age groups (e.g., 18–30, 31–45).

### **Step 4: Exploratory Data Analysis (EDA)**
- **Visualize data trends**:
  - Histograms for `athlete_average_speed` distribution.
  - Box plots and violin plots for comparisons across seasons, genders, and race lengths.
  - Scatterplots to analyze relationships between age and speed.

### **Step 5: Insights and Answering Business Questions**
- Use group-by operations and descriptive statistics to extract insights.
- Answer business-relevant questions such as:
  - How do seasons affect performance?
  - Which age groups perform best in ultra-marathons?
  - Are athletes slower in summer compared to winter?

---

## Business Questions to Answer
This project addresses the following questions:
1. **Which countries host the fastest ultra-marathons?**
2. **Are athletes slower in summer compared to winter?**
3. **How does performance vary between different race distances (e.g., 50km, 50mi)?**
4. **Which age groups perform best in ultra-marathons?**
5. **What are the gender differences in ultra-marathon performance?**
6. **For 50mi races, how does performance vary across seasons?**

---

## Skills Used

### **Data Manipulation**
- **Pandas**: Cleaning, filtering, and aggregating data.
- Group-by operations for calculating statistical summaries.

### **Data Visualization**
- **Seaborn** and **Matplotlib**:
  - Histograms, box plots, violin plots, and scatterplots.

### **Data Cleaning**
- Handling missing values.
- Removing invalid data (e.g., unknown genders).
- Transforming raw data into structured formats (e.g., seasons, age groups).

### **Exploratory Data Analysis (EDA)**
- Identifying trends, patterns, and outliers.
- Answering business questions using descriptive statistics and visualizations.

### **Communication**
- Presenting results through clear visuals and actionable insights.

