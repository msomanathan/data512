# Homework 1
The goal of this homework is to collect user page views data of several dinosaur pages in Wikipedia, and analyze the pages that are visited most often. In addition, we also analyze the pages least popular. The data is a time series from January 2015 to September 2022.

## Data source
- The list of dinosaur articles is available in the file `dinosaur_articles.csv`. This was obtained from https://docs.google.com/spreadsheets/d/1zfBNKsuWOFVFTOGK8qnTr2DmHkYK4mAACBKk1sHLt_k/edit?usp=sharing.
- The source data for Wikipedia pages is from the REST API documented in https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews. The API usage license and terms are available in https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions.

## Code
The code is provided in the notebook `article_pageviews.ipynb`.

## Output files
The code generates the following output files:
- `dino_monthly_desktop_201501-202209.json`, which is monthly page views on desktop
- `dino_monthly_mobile_201501-202209.json`, which is monthly page views on mobile
- `dino_monthly_cumulative_201501-202209.json`, which is monthly page views on desktop and mobile combined
- `MaximumAndMinimumAverage.png`, which is the plot for max and min viewed articles by access type
- `top10.png`, which is the plot for top 10 viewed articles by access type
- `fewest10.png`, which is the plot for fewest 10 viewed articles by access type
