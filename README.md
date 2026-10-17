# 🎬 Netflix Movies & TV Shows Data Cleaning & Exploratory Data Analysis (EDA)

**AnalystLab Africa Data Analytics Internship | Week 2**
Prepared by **Zainab Danjuma**

## Overview

This project cleans, validates and explores the Netflix Movies & TV Shows dataset to turn raw catalogue data into an analysis-ready dataset and to uncover insights about content mix, growth, geography, audience ratings and genres.

## Business Problem

Streaming catalogue data is messy: directors, casts and countries are often missing, dates are stored as text, and fields mix formats. Before any content-strategy question can be answered (What is the Movie/TV Show mix? How fast did the library grow? Which markets and genres lead? Who is the content for?), the data has to be cleaned and validated.

## Dataset

| Item | Detail |
|---|---|
| File | `netflix_titles.csv` |
| Raw size | 8,807 rows x 12 columns |
| Cleaned size | 8,790 rows x 12 columns |
| Primary key | `show_id` |
| Columns | show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description |

## Tools

Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

## Data Cleaning

| Issue | Action |
|---|---|
| Missing `director` (29.91%), `country` (9.44%), `cast` (9.37%) | Filled with `"Unknown"` |
| Missing `date_added` (10), `rating` (4), `duration` (3) | Rows removed (17 rows in total) |
| Duplicate records | None found |
| Column names | Stripped, lowercased, spaces replaced with underscores |
| `date_added` stored as text | Converted to `datetime64` with `pd.to_datetime()` |
| Validation | Checked type, rating, duration and release year; no invalid values |

## Key Insights

- Movies make up about 70% of the catalogue (6,126 titles) and TV Shows about 30% (2,664) because Netflix built breadth through films first.
- Additions rose from 82 titles in 2015 to a peak of 2,016 in 2019, reflecting rapid global expansion; 2021 is a partial year (data ends 25 September 2021).
- The United States (3,680), India (1,046) and the United Kingdom (803) are the top content-producing countries.
- TV-MA and TV-14 cover about 61% of titles because the platform is aimed mainly at adult and teen viewers; content for young children is about 10%.
- International Movies (2,752), Dramas (2,426) and Comedies (1,674) are the top genres.

## Recommendations

1. Continue investing in international content, as it remains one of the platform's strongest categories.
2. Expand investment in emerging markets to diversify the content library.
3. Balance mature-rated content (about 61% of titles) with family and kids programming (about 10%) to appeal to a wider subscriber base.

## Next Steps

- Track additions over a full 2021, since the data ends in September.
- Pair this catalogue data with viewership data to find expansion opportunities.

## Limitations

- Catalogue snapshot only: no viewership, scores or revenue, so popularity cannot be measured.
- 2021 is a partial year.
- Multi-country and multi-genre titles are counted once per tag.

## Repository Structure

```
Netflix-EDA/
|-- Data/
|   `-- netflix_titles.csv
|-- Netflix_Data_Cleaning_EDA.ipynb
|-- Netflix_Cleaned.csv
|-- Netflix_EDA_Report.pdf
`-- README.md
```

## How to Run

1. Clone the repository.
2. Install the libraries: `pip install pandas numpy matplotlib seaborn jupyter`
3. Update the file path in the notebook's load cell to point to `Data/netflix_titles.csv`.
4. Run all cells in `Netflix_Data_Cleaning_EDA.ipynb`.

## Author

**Zainab Danjuma**: Data Analytics intern, AnalystLab Africa
