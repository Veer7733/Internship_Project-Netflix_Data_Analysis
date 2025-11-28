# Internship_Project-Netflix_Data_Analysis

Comprehensive data-driven analysis of Netflix content (movies & TV shows) to uncover trends in genres, ratings, release patterns, and predict content type using machine learning.

---

## Project Overview

This project analyzes the full Netflix titles dataset (2008–2021) to understand content distribution, popularity trends across genres, ratings, and geographic origin — and builds a predictive model to classify whether a title is a **Movie** or a **TV Show** based on metadata. It demonstrates data cleaning, exploratory data analysis, feature engineering, visualization, and machine-learning skills.

---

## Data Summary

| Attribute | Details |
|-----------|---------|
| **Dataset timeframe** | 2008 – 2021 (oldest title: 1925) |
| **Number of records** | ~8,800 (combined movies & TV shows) |
| **Key columns** | `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in` (genres), etc. |
| **Processed & cleaned** | Removed duplicates, handled missing values, parsed dates, extracted genres, duration, release info, engineered new features |

---

## Key Insights & Findings

### Content Distribution  
- Movies far outnumber TV Shows overall — but TV Show releases have surged since 2018.  
- Genre-wise: International Movies, Dramas, Comedies, Action & Adventure dominate.  
- Geographically, **USA** leads, followed by **India** and other countries in content count.  

### Ratings & Audience  
- Most common rating: **TV-MA** (Mature), followed by TV-14 and TV-PG — indicating a significant portion of content targets mature audiences.  

### Temporal Trends  
- Peaks in content additions around **July** and **December**, possibly coinciding with holidays or global releases.  
- TV Show additions show strong upward trend from 2018–2020.

---

## Methodology

### 1. Data Cleaning & Preprocessing  
- Converted `date_added` to datetime, extracted `year`, `month`.  
- Split multi-valued fields like `listed_in` into individual genres.  
- Parsed `duration` to extract numeric duration (minutes or number of seasons).  

### 2. Feature Engineering  
- Derived features such as `duration_time`, `is_season` (flag if TV show), `cnt_genres`, and encoded categorical features (rating, country, etc.).  

### 3. Exploratory Data Analysis (EDA) & Visualization  
- Plots for content type distribution, rating distribution, genre frequency, country-wise content count, release trend over years/months.  
- Visual insights on which genres, countries, or ratings dominate — useful for strategic insights/recommendations.  

### 4. Machine Learning: Content Type Classification  
- Model used: **Random Forest Classifier**  
- Train/Test split: 80/20 (with stratification)  
- Features: Metadata only (duration, release year, genre count/indicator, rating, etc.)  
- Achieved good accuracy on test set — demonstrating clear separability of movies vs TV shows with chosen features.

---

## Tech Stack

| Purpose         | Technology / Library |
|-----------------|---------------------|
| Data Manipulation | Python, Pandas, NumPy |
| Data Visualization | Matplotlib, Seaborn |
| Modeling / ML   | Scikit-learn (RandomForestClassifier) |
| Notebook        | Jupyter Notebook |

---

##  How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/Veer7733/Internship_Project-Netflix_Data_Analysis
   ``` 
2. Navigate to the project folder:
   ```bash
   cd Internship_Project-Netflix_Data_Analysis
   ```
3. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
4. Open the Jupyter Notebook:
   ```bash
   jupyter notebook Netflix Data_ Cleaning, Analysis and Visualization.ipynb
   ```
