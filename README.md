# What makes Netflix content successful?
A data visualisation project analysing what makes content successful on Netflix, focusing on global production patterns, quality metrics, and genre performance.

## 📊 Project Overview

This project examines Netflix's content catalogue from 2001 to 2021 to uncover success patterns for content strategists. Using data visualisation principles, I explore:
- Regional content production landscape
- Variations in regional content quality 
- Content originating from Asia and their genre specialisation

This was created as part of my individual assignment from the Data Science: Visualization and Analytics in R (DSVAR) course, December 2025. 

**Target Audience:** Content strategists and entertainment industry professionals

## 🎯 Key Questions

- Exploration: How has Netflix content production evolved across different regions over time (2001-2021)
- Explanation: Did North America's declining share occur because other regions improved in quality?
- Drill-down Exploration: Which specific Asian countries are driving the region's content expansion?
- Explanation: Which genres are driving quality in these Asian countries?   

## 📁 Dataset

**Source:** [Netflix TV Shows and Movies Dataset](https://www.kaggle.com/datasets/victorsoeiro/netflix-tv-shows-and-movies) from Kaggle

**Contains:** 5,850+ titles with 15 variables including:
- Title information (name, type, release year)
- Quality metrics (IMDB score, votes, TMDB scores)
- Production details (countries, genres, runtime)
- Audience specifications (age certification)

## 🛠️ Tools & Technologies

- **R** - Data analysis and visualization
- **tidyverse** - Data manipulation (dplyr, tidyr)
- **ggplot2** - Data visualization
- **RMarkdown** - Reproducible reporting

## 📈 Visualisations

1. **Regional Production Landscape** - Bar chart showing content distribution by region
2. **Quality by Region** - Line chart showing IMDB scores across regions over a 20-year horizon
3. **Quantity by Asian countries** - Area chart showing number of titles released in Asia
4. **Genre Performance** - Faceted bar chart identifying high-performing genres

In addition to the 4 visualisations, there are short justifications under each visualisation explaining how I accounted for visual literacy and trade-offs in view, focus, and sequence of congruence.
## 🔍 Key Insights

- While North America historically dominated Netflix content production, European and Asian content achieved quality parity post-2015.
- India, Japan and South Korea are the primary drivers behind the rapid Asia content expansion. 
- These successful Asian countries excel by specialising in specific genres rather than competing across all categories:
  - Japan dominates in animation
  - South Korea excels in dramas

## 📝 Methodology

**Import, then Wrangle**: 
I imported the Netflix titles dataset (titles.csv) containing 5,850 titles with 15 variables including release year, production countries, genres, runtime, and IMDb scores. The dataset required preprocessing to handle multi-value fields:

1. **Primary production country extraction**: Used string manipulation to extract the first country from the production_countries list field, as titles often had multiple production countries listed
2. **Primary genre extraction**: Extracted the first genre from the genres list field to focus on primary content classification

As part of data preprocessing, I also **mapped individual countries into seven geographical regions** (North America, Europe, Asia, Latin America, Middle East, Africa, and Oceania) to enable macro-level analysis.

**Analytical Approach:**
I employed a **sequential exploratory-explanatory framework** to move from broad patterns to specific insights:

- Time Horizon: Focused on 2001-2021 releases to capture Netflix's global expansion era while excluding sparse early years and incomplete 2022 data
- Broad-to-Narrow Analysis: Progressed from regional overview → cross-regional quality comparison → within-region country analysis → genre specialisation patterns
- Quality classification: Defined IMDb scores of 7.0 and above as a quality threshold to identify high-performing content

**Visualisation Design Principles:**
This analysis follows the Grammar of Graphics framework and data visualisation best practices from Kieran Healy's *Data Visualization: A Practical Introduction*.

## 📂 Repository Structure
```
├── netflix_analysis.Rmd          # Main analysis file
├── titles.csv                     # Dataset
├── README.md                      # This file
└── figures/                       # Generated visualizations
```
