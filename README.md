# Collaborative Data Wrangling & Exploratory Data Analysis (Spotify Dataset)
Readme file prepared by: Eva Kaushik

## Project Overview
This project demonstrates collaborative data wrangling, cleaning, and exploratory data analysis (EDA) using a Spotify dataset. The primary goals were to practice reproducible workflows, version control with Git/GitHub, and apply both fundamental and advanced EDA techniques.

We explored track-level audio features, cleaned and standardized the dataset, and applied advanced methods such as **dimensionality reduction (PCA), clustering, and predictive modeling** for popularity classification.

## Repository Structure

```
Collaborative-Data-Wrangling-EDA/
│── data/
│   └── spotify_cleaned.csv and spotify.csv(original)     # Cleaned dataset (raw excluded)
│── notebooks/
│   └── Main-EDA.ipynb             # Exploratory Data Analysis and Advanced EDA + Pattern Recognition
│── CONTRIBUTIONS.md               # Team contributions
│── README.md                      # Project description & guide
│── requirements.txt               # Dependencies
```

## Dataset

1. Source: [Spotify Tracks Dataset (Kaggle)](https://www.kaggle.com/datasets/zaheenhamidani/ultimate-spotify-tracks-db) |232k tracks | Size: 33.71 MB | Rows: ~23k[open-access] | Cleaned dataset: less than 17k rows
2. Accessed: September 2025
3. Description:
  Each row represents a song/track with audio features extracted from Spotify’s API.
  Features include:
  * *Categorical*: `genre`, `artist_name`, `track_name`, `track_id`
  * *Numerical*: `popularity`, `acousticness`, `danceability`, `energy`,
    `instrumentalness`, `key`, `liveness`, `loudness`, `mode`, `speechiness`,
    `tempo`, `time_signature`, `valence`, `duration`, `duration_min`

## Data Cleaning 
Performed by: Eric 

1. Removing missing values, duplicacies and printing cleaned values.
2. Printing heatmap with correlation.

# Data Pre-Processing
Performed by: Eva Kaushik

1. Standardized column names → lowercase, replaced spaces with underscores.
2. Removed duplicates (based on `track_id`).
3. Converted duration from seconds → minutes (float, 2 decimals).
4. Checked categorical consistency for `key`, `mode`, `time_signature`.
5. Saved cleaned dataset to `/data/spotify_cleaned.csv`.

## Exploratory Data Analysis (EDA)
Performed by: Eva Kaushik

Descriptive Statistics: Mean, median track duration; feature correlations.
Visualizations:

  * Histogram of track duration.
  * Scatterplot of *danceability vs. energy*.
  * Correlation heatmap of audio features.


## Advanced EDA & Modeling
Performed by: Eva Kaushik

* **Genre Fingerprinting**: PCA projection to 2D space, visualizing genre clusters.
* **Centroid Analysis**: Comparing genre centroids in PCA space.
* **Predictive Modeling**:

  * Classified tracks into *low/medium/high popularity buckets*.
  * Applied **Random Forest Classifier** with **oversampling (SMOTE)** for class balance.
  * Evaluated performance with precision, recall, F1-score.

## Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

**Key libraries**:
* `pandas`, `numpy`
* `matplotlib`, `seaborn`
* `scikit-learn`
* `imbalanced-learn`

## Deliverables Checklist
1. `data/` with cleaned dataset
2. `notebooks/` with analysis code
3. `README.md` (this file)
4. `CONTRIBUTIONS.md` file
5. Version control with multiple commits + pull requests

## License
This project is licensed under the **GNU GPL-3.0 License**.
