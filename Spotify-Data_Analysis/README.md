# Spotify Data Analysis

## Overview

This data analysis project investigates how track popularity, artist collaborations, and musical attributes influence listener engagement on Spotify. By analysing multiple datasets — including a supplemental one from Kaggle — I examined three core questions:

1. How do hit tracks influence the success of other tracks in the same album?
2. Do artists change their musical style in collaborations compared to solo performances?
3. Do popular tracks align or diverge musically from other tracks on the album?

## Subtopics & Findings

### 1. Influence of Popular Tracks on Albums

- Goal: Determine whether popular tracks boost the overall performance of their albums.
- Approach: Defined popularity threshold (`popularity ≥ 80`), removed duplicates, and excluded singles and corrupted entries.
- Key Insights:
  - Albums containing one or more popular tracks had significantly higher average popularity, stream count, and playlist presence.
  - Popular tracks drive album engagement.

### 2. Solo Artists vs. Collaborations

- Goal: Explore how musical attributes shift in collaborations.
- Approach: Identified collabs by parsing artist names (e.g., "Feat." or “;”), excluded remixes and invalid genres.
- Key Insights:
  - Artists often change genres in collaborations (e.g., classical to pop).
  - Musical elements like danceability and loudness changed most; energy remained consistent.
  - Collaborations affect genre choice more than core musical attributes.

### 3. Hit Tracks vs. Album Cohesion

- Goal: Compare musical attributes of popular tracks to other songs on the same album.
- Approach: Focused on albums with at least one hit (`popularity ≥ 80`) and visualized attribute distributions via density plots.
- Key Insights:
  - Popular tracks had:
    - Higher energy and loudness
    - Tighter valence distributions
  - Liveness did not show a meaningful correlation.
  - Musical traits like energy and loudness help predict popularity.

## Datasets Used

- Primary Spotify Dataset: Included track attributes, artist names, and genres.
- Supplementary Kaggle Dataset: Contained stream counts, chart ranks, and playlist appearances.
- Cleaned and merged overlapping entries from both datasets.

## Tools & Technologies

- Python  
- Pandas & NumPy  
- Matplotlib & Seaborn  
- Jupyter Notebook  

## Data Cleaning & Challenges

- Duplicates: Same tracks appeared under different IDs — averaged popularity values.
- Invalid Entries: Removed tracks with corrupted characters or non-existent Spotify listings.
- Ambiguity in Genres: Dropped entries with numeric or irrelevant genre labels.
- Excluded:
  - Singles with no album association
  - Remixes and mashups
  - Outliers with unusual characters


## Visualizations

- Histograms comparing album-wide impact of popular tracks  
- Line graphs showing genre changes in collaborations  
- Density plots for musical attribute overlaps

Appendices A, B, and C contain detailed visualizations and threshold logic.


## Limitations

- Spotify personalization may introduce duplicates across albums.
- Playlist algorithms are complex and sometimes genre- or mood-based, not strictly popularity-based.
- Genre mislabeling and numeric genres reduced reliability in genre-based analysis.
- Remixes could falsely represent musical shifts and were excluded.
