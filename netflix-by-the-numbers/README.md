# Netflix Shows - Exploratory Data Analysis (EDA)

This repository contains a detailed exploratory data analysis of the [Netflix Movies and TV Shows dataset](https://www.kaggle.com/datasets/shivamb/netflix-shows). The goal is to uncover trends, insights, and opportunities in Netflix's content catalog to inform strategic decisions in content production, acquisition, and marketing.

---

##  Dataset Overview
- **Source:** [Kaggle - Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows)  
- **Entries:** 8,807  
- **Features:** 15 (including title, director, cast, country, release year, rating, duration, genres, etc.)

---

##  Key Insights

### Content Type Distribution
- **Movies:** 6,131  
- **TV Shows:** 2,676  

### Release Year Trend
- Content ranges from **1925 to 2021**  
- **Peak year:** 2018, with **1,147 titles** added  

### Duration Analysis
- **Movies:** Average ~99.6 minutes  
- **TV Shows:** Average ~1.8 seasons  

### Geographic Distribution
- **Top country:** United States (2,818 titles)  
- U.S. dominates both Movies and TV Shows  

### Ratings
- **Most common rating:** TV-MA (3,207 titles)

### Top Creators
- **Most featured director:** Rajiv Chilaka (19 titles)

---

##  Data Cleaning
- Handled missing values via deletion (for high-null columns) or imputation  
- Converted data types (e.g., dates, durations)  
- Removed duplicate records  

---

##  Recommendations

1. **Content Strategy**
   - Expand **TV Show offerings** to diversify the library  
   - Leverage country-level insights to guide regional content strategies  

2. **Data Enrichment**
   - Fill missing values in `director`, `cast`, `country`, and `date_added` to improve analysis depth  

3. **Outlier Analysis**
   - Validate unusual movie durations to spot possible data entry errors  

4. **Feature Engineering**
   - Extract and analyze individual genres from `listed_in`  
   - Break down `cast` and `director` for network and frequency analysis  
   - Use `description` for NLP-based content modeling  

5. **Genre and Tag Analysis**
   - Identify underrepresented genres for growth opportunities  
   - Explore trending and historically popular categories

---

##  Deliverables

-  Jupyter Notebook(s) with complete EDA workflow  
-  Visualizations (plots, heatmaps, bar charts)  
-  Executive Summary with business recommendations  
-  Cleaned, analysis-ready dataset  

---



