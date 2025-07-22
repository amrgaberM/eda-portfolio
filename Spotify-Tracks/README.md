# Spotify Tracks Dataset (1921–2020) - Exploratory Data Analysis

## Overview

This project presents an exploratory data analysis (EDA) of a dataset containing over 156,000 Spotify tracks spanning the years 1921 to 2020. The dataset includes various audio features such as danceability, energy, loudness, acousticness, and popularity, among others.

The goal of this EDA is to uncover patterns, trends, and relationships within the dataset and lay the groundwork for future modeling tasks such as predicting track popularity.

---

## Summary of Findings

- The dataset includes over 156,000 tracks with no duplicate entries.
- A small number of missing values were identified in the `popularity`, `release_date`, `speechiness`, and `tempo` columns. These represent a very small portion of the data and can be handled via imputation or removal.
- The `release_date` column was successfully converted to datetime, enabling time-series analysis.
- Univariate analysis showed:
  - Distribution of various audio features.
  - Most common artist and track name occurrences.
  - A sharp increase in the number of tracks in recent years.

- Multivariate analysis revealed:
  - A strong positive correlation between `year` and `popularity`.
  - Significant negative correlation between `acousticness` and `energy`.
  - Positive correlation between `energy` and `loudness`.
  - Varying popularity scores across artists.
  - Over time, tracks have become less acoustic and more energetic and loud.
  - Some relationships exist between popularity and audio features, but many are weak or widely dispersed.
  - Differences were observed in feature distributions between major (mode = 1) and minor (mode = 0) key tracks.

- Outlier analysis using the IQR method identified outliers in columns such as `instrumentalness`, `speechiness`, and `explicit`.

---

## Recommendations

1. **Address Missing Values**  
   Consider simple imputation (mean or median) or row removal for `popularity`, `release_date`, `speechiness`, and `tempo` depending on the context.

2. **Handle Outliers**  
   For analyses sensitive to extreme values, apply appropriate outlier treatment methods such as transformation, capping, or exclusion.

3. **Deeper Correlation Analysis**  
   Investigate the relationship between `year` and `popularity` more thoroughly. Determine whether popularity trends are due to platform dynamics, artist activity, or other features.

4. **Artist-Level Exploration**  
   Identify characteristics that distinguish high-performing artists. Analyze their audio profiles, release timing, and volume of content.

5. **Time-Series Analysis**  
   Leverage the `release_date` column to explore time-based patterns in audio features and track popularity.

6. **Feature Engineering**  
   Introduce new features such as `decade`, `track_age`, or artist-level aggregations to enhance potential predictive models.

7. **Model Building**  
   Use the insights from EDA to inform the development of regression or classification models aimed at predicting track popularity or clustering audio features.

---

## Next Steps

- Build a regression model to predict track popularity based on audio features and metadata.
- Apply clustering techniques (e.g., K-Means) to group tracks with similar characteristics.
- Visualize popularity and audio trends across decades.

---

## Dataset Source

- [Spotify Dataset (1921–2020) - 160k+ Tracks on Kaggle](https://www.kaggle.com/datasets/yamaerenay/spotify-dataset-1921-2020-160k-tracks)

