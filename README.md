# Animation Movies Exploratory Data Analysis
This repository contains summary about my project for Global AI Hub Aygaz Data Science Bootcamp.

![image](https://www.vancouversymphony.ca/site-content/uploads/2024/03/Shrek2-Secondary07-scaled.jpg)

## About Dataset
The dataset used contains various information about approximately 52,000 animated films from past to present. If you would like to work with same dataset, it can be found [here](https://www.kaggle.com/datasets/asaniczka/52000-animation-movie-details-dataset-2024).

Grab one or two buckets of popcorn along with your favourite drink and head to [my notebook on Kaggle](https://www.kaggle.com/code/talhapekdemir/global-ai-hub-exploratory-data-analysis-bootcamp).

### Dataset Variables
- id: TMDB id of the movie
- title: Release title of the movie
- vote_average: Average points received over ten.
- vote_count: Total people voted
- status: Status of the movie (eg. in production, released)
- release_date: The date of the movie in theatres
- revenue: Total revenue of the movie
- runtime: Total runtime of the movie
- adult: If the movie contains adult content
- backdrop_path: URL of the movie backdrop image
- budget: Total budget of the movie
- homepage: Homepage url for the movie
- imdb_id: IMDB id of the movie
- original_language: The language of the movie originally released
- original_title: Title of the movie originally released
- overview: Summary or overview of the movie
- popularity: Popularity score of the movie
- poster_path: URL of the movie poster
- tagline: Tagline or the slogan of the movie
- genres: Genre of the movie
- production_companies: Company/companies the movie producted by
- production_countries: Country/countries the movie producted at
- spoken_languages: The languages spoken in the movie

### Libraries Used
- pandas
- numpy
- scipy
- matplotlib
- seaborn
- missingno

### Key Findings
- id is unnecessary.
- Dataset has 51945 rows and 23 columns.
- After filling missing and some feature engineering dataset left with 51944 rows and 19 columns.
- title, backdrop_path, homepage, original_title, overview, poster_path and tagline are unique string variables. Some of them are missing rows largely.
- status, adult, original_language categorical with one value each row.
- spoken_languages, production_countries, production_compaies and genres are categorical too but have comma seperated sub categories.
- release date is object.
- Rest of the columns are numeric.
- After adding random missing values to rows some column value types have changed. Corrected them all in data cleaning phase.
- In one hand some movies have colossal budgets and revenues in the other hand there are movies with no budget and revenue.
- Most of the movies are not voted hence have no average. Minimum is 0 points, maximum is 10 with 2,6 mean.
- Most voted movie is Inside Out and has 19463 votes.
- Most earned movie is Frozen 2 and grossed 1.45 billion dollars. Highest budget is 2.6 billion dollars and it belongs to Tangled.
- The dataset contains TV series too not only movies. So the animation with longest secreentime is 3.720 minutes.
- There are total of 19 unique genres, 101 unique original languages, 155 unique production countries and 10930 production companies.
- Only 1.4% of animations has adult content.
- Comedy, family and fantasy are the top 3 sub genres.
- Only 15.7% of the movies have a homepage.
- Only 9% of the movies have a slogan.
- 87.4% of the movies have an overview.
- 72.3% of the movies have a poster.
- 56.3% of the TMDB animation movies present in IMDB.
- 54% of the movies are released in English. Japanese and French is trailing. Top production countries are USA, Japan and France.
- ONF | NFB is the studio with most animation movies. Walt Disney Productions and Soyuzmultfilm are trailing.
- Despite Frozen 2 beşng the top grossed, Elemental is the  most popular animation.
- Most animations released around 2020.
- In the charts popularity of the animations seems like dropping after a significant spike. But that could be about the pandemic or the dataset itself since dataset contains mostly relevant animations (prior to 10 months) and still there is unreleased ones.
- Found duplicated values and removed.
- Columns homepage, tagline, overview, imdb_id, poster_path, backdrop_path, removed and used missing values to augment dataset. status is irrelevant since release_date is present. spoken_languages is is irrelevant too. Original language is present and one of them full language name but other one is simply language codes. Converting all to one another too much of a hassle.

