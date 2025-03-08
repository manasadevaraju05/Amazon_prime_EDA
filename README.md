# Amazon_prime_EDA
This repository contains an Exploratory Data Analysis (EDA) of Amazon Prime titles using Python libraries such as Pandas, Matplotlib, and Seaborn. The analysis covers data cleaning, handling missing values, visualization of content types, and insights into country-wise distributions, release years, and more.
Amazon Prime EDA Analysis
# Amazon Prime EDA Analysis
A detailed Exploratory Data Analysis (EDA) of Amazon Prime Video dataset using Python, Pandas,
and Matplotlib.
## Table of Contents
1. Project Overview
2. Dataset Information
3. Technologies Used
4. Key Insights
5. Code and Analysis
6. Conclusion
## 1. Project Overview
This project focuses on performing Exploratory Data Analysis (EDA) on Amazon Prime Video
dataset to uncover insights about content type, genres, release trends, and more.
## 2. Dataset Information
- Dataset Name: amazon-prime-titles.csv
- Columns:
- type - Movie or TV Show
- title - Name of the content
- director - Director's name
- cast - List of actors
- country - Country of production
- date_added - Date content was added
- release_year - Year of release
- rating - Content rating (e.g., PG, R)
- duration - Length of content
- listed_in - Genres
- description - Brief summary
## 3. Technologies Used
- Programming Language: Python
- Libraries:
- pandas for data manipulation
- matplotlib and seaborn for data visualization
- numpy for numerical operations
## 4. Key Insights
- Content Distribution:
- Majority of content is Movies.
- TV Shows are significantly fewer.
- Popular Genres:
- Drama, Comedy, and Action are the most listed genres.
- Release Trends:
- Significant increase in content after 2015.
- Top Countries:
- USA, India, and UK dominate content production.
## 5. Code and Analysis
### a. Importing Libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
### b. Loading the Dataset
df = pd.read_csv('amazon-prime-titles.csv')
df.head()
### c. Data Cleaning
- Filling Missing Values:
df.fillna('Unknown', inplace=True)
- Checking Missing Values:
df.isnull().sum()
### d. Data Visualization
*Content Type Distribution:*
content_counts = df['type'].value_counts()
content_counts.plot(kind='bar', title='Distribution of Content Types on Amazon Prime')
plt.xlabel('Content Type')
plt.ylabel('Count')
plt.show()
### e. Release Year Trend:
plt.figure(figsize=(12, 6))
sns.countplot(data=df, x='release_year', order=df['release_year'].value_counts().index[:20])
plt.title('Top 20 Release Years on Amazon Prime')
plt.xticks(rotation=45)
plt.show()
## 6. Conclusion
- Amazon Prime has a higher count of Movies compared to TV Shows.
- Post-2015 saw a surge in content releases.
- Drama and Comedy are the most common genres.
