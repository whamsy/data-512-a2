# data-512-a2
DATA 512 A2

## Bias in Data

Name: Vamsy Atluri
Date: 8 Nov 2018

## Goal

The goal of this assignment was to analyze the quanity and quality of politicial articles on Wikipedia on a geographical basis, and in the process try to understand bias, its causes and consequences.

## Data sources

2 external data sources were used:

    1. Article data: https://figshare.com/articles/Untitled_Item/5513449 
    This data contains information about the various political pages on Wikipedia, the country it realtes to and a revision_id

    2. Population data: https://www.dropbox.com/s/5u7sy1xt7g0oi2c/WPDS_2018_data.csv?dl=0 
    This data contains information about geograhical entities (mostly countries) and their populations.

## Output

One of the outputs of the exercise was a csv file ('final_data.csv) that combines the two inputs along with a Article Quality Score.

It has the following columns:

| Column | Description |
|--------|-------------|
| country | Country name |
| article_name | The name of the article |
| revision_id | Revision_id of the article from Wikipedia |
| article_quality | Quality of the article as determined by the ORES API |
| population | The population of the country |



Wikimedia ORES API: https://www.mediawiki.org/wiki/ORES 
Provides a prediction for the article's quality class
Library versions
Python: 3.6.2
requests: 2.18.4
json: 2.6.0
pandas: 0.22.0
matplotlib: 2.0.2
Output
The data from the three sources listed about is joined into a 
single dataframe, and is stored in the data-processed folder.

The final dataframe contains following columns: 
page    country    rev_id    population    predictions

Tables
10 highest-ranked countries: Ratio of politician articles to country population


### 10 lowest-ranked countries: ratio of article quality to article count


### 10 lowest-ranked countries: ratio of article quality to article count


### 10 highest-ranked countries: ratio of article quality to article count


Reflections
What biases did you expect to find in the data, and why?
I expected to see higer quality articles in english speaking regions given that 
most Wikipedia are in English. I also expected to see the quality of article being 
proportional to the economic development of a country, given that access to internet 
could be a barrier in some regions.

What are the results?
The list of countries with least number of articles per capita isn't very surprising 
given the large population of China and India. Also, the list of countries with most 
articles per captia a highly skewed towards very small countries.

The tables relating to the quality of articles is more surprising, however. There are a lot 
of countries which do not have any article classified as 'good'. The countries with a high 
proportion of good quality articles are also not the ones I'd expected to see. (USA, countries 
in europe)

What theories do you have about why the results are what they are?
The 'ratio of articles to population' tables are highly skewed, most likely due the effect of 
population on the ratio. In the second set of tables where we compare the quality to the count of articles, it looks like 
the regions with low total article counts domniate the top-10 list (few articles, but well 
written, resulting in a high ratio)

License
This assignment is released under the MIT license.

The data located on figshare is licensed under CC. 
The license for population data on dropbox is unknown. 
The ORES API also licensed under CC.
