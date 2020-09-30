# Powerlifting Data Science Project
**Goal:** To predict the squat, bench, and deadlift (DVs) of powerlifters
* Scraped ~10,000 powerlifting records and competition histories from 1000s of interconnected URLs using Selenium and BeautifulSoup
* Imputed nulls with MICE
* Engineered 12 new columns, such as average competition sq/bn/dl, average rate of change in sq/bn/dl, and second best competition sq/bn/dl
* CatBoost encoded all categorical variables
* Optimized Multiple Linear Regression, Lasso, and Random Forest Regressor...
* Productionized...

## Technologies
**Packages:** pandas, numpy, matplotlib, seaborn, sklearn, selenium, flask, pickle


## Web Scraping
Using Selenium and BeautifulSoup, I scraped data off openpowerlifting.org and data from the associated links to each powerlifter's competition history.

26 columns:
* **Provided data:** *Federation, Date, Location, Sex, Age, Equip, Class, Weight, Squat, Bench, Deadlift, Total, Dots (score)*
* **Engineered columns from competition history:** *Squat average across previous competitions excluding the best, Bench average excluding best, Deadlift average excluding best, Squat average standard deviation, Bench average standard deviation, Deadlift average standard deviation, Second best squat, Second best bench, Second best deadlift, Squat average rate of change, Bench avg. rate of change, Deadlift avg. rate of change, Count of competition history*

## Data Cleaning
* Dropped duplicate powerlifters
* Filled missing Class values by calculating from Weight
* Recoded columns types
* Imputed remaining nulls with MICE

## Feature Engineering
* CatBoost encoded all categorical variables
* Engineered 6 new columns: month, season, year, country, state, number of records in past year of the same class, number of days since last record in the same class

## Exploratory Data Analysis
* Observed the distributions of continuous variables and the counts of categoricals
* Created scatterplots of each continuous variable against the DVs, as well as correlation dataframes
* Created box and violin plots of categorical variables against the DVs, as well as pivot tables
* Ran Kruskal-Wallis H-tests to observe if differences exist in the medians

## Model Building


## Productionizing

