# Homework 2
The goal of this assignment is to explore the concept of bias in data using Wikipedia articles. This assignment will consider articles on political figures from different countries.

## Data source
- The list of politician articles is available in the file `politicians_by_country_SEPT.2022.csv`. This file was was downloaded from https://docs.google.com/spreadsheets/u/0/d/1Y4vSTYENgNE5KltqKZqnRQQBQZN5c8uKbSM4QTt8QGg/edit, which is based on the [politicians by nationality](https://en.wikipedia.org/wiki/Category:Politicians_by_nationality) data crawled from Wikipedia articles.
- The data for population by country and region is available in the file `population_by_country_2022.csv`. This file was downloaded from https://docs.google.com/spreadsheets/u/0/d/1POuZDfA1sRooBq9e1RNukxyzHZZ-nQ2r6H5NcXhsMPU/edit, which is based on the [world population data sheet](https://www.prb.org/international/indicator/population/table/) published by the Population Reference Bureau.

## Code
The code is provided in the notebook `hw2.ipynb`. The code uses the following public APIs to query for the Wikipedia article revision ID, and the associated article quality predictions:
- Article Revision ID: The [API:Info](https://www.mediawiki.org/wiki/API:Info) request returns the latest revision ID for a given Wikipedia article.
- Article Quality: The [ORES](https://www.mediawiki.org/wiki/ORES) machine learning system exposes an API to query for the article quality for a given article and revision ID. The article prediction values can be one of - FA, GA, B, C, Start, Stub. FA and GA are considered high quality, and the rest are considered low quality. For more information regarding the article quality descriptions, please refer to [Wikipedia:Content Assessment](https://en.wikipedia.org/wiki/Wikipedia:Content_assessment) procedures.

## Output files
The code generates the following output files:
- `wp_countries-no_match.txt` - A list of countries that did not have a matching population data.
- `wp_politicians_by_country.csv` - A list of politician articles along with the country, region, population, article revision ID, and article quality.

## Results
The code generates the following 6 tables analyzing the countries/regions with the highest/lowest quality articles, and the total number of articles per capita.
- Top 10 countries by coverage: The 10 countries with the highest total articles per capita (in descending order).
- Bottom 10 countries by coverage: The 10 countries with the lowest total articles per capita (in ascending order).
- Top 10 countries by high quality: The 10 countries with the highest high quality articles per capita (in descending order).
- Bottom 10 countries by high quality: The 10 countries with the lowest high quality articles per capita (in ascending order).
- Geographic regions by total coverage: A rank ordered list of geographic regions (in descending order) by total articles per capita.
- Geographic regions by high quality coverage: Rank ordered list of geographic regions (in descending order) by high quality articles per capita.

## Research Implications
- From the results, it appears that the countries in the Caribbean islands have both highest, as well as, lowest number of articles per capita.
- High quality articles seem to be from the European countries.
- Africa, Asia, and Caribbean seem to have the most low quality articles.
