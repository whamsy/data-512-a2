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

## Other Resources

To determine the quality of articles, the Wikimedia ORES API was used (https://www.mediawiki.org/wiki/ORES).

It gives a measure of probability as to which class the article would best fit in. While complete information cane be obtained on the website,
for the purpose of this assignment articles predicted with a high degree of probability to belong to FA or GA classes are considered high
quality articles.

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


This csv file is used for further analysis as shown in the ipython notebook (Data_512_A2.ipynb).

## Library versions

Python: 3.6.5
requests: 2.18.4
pandas: 0.23.0
matplotlib: 2.2.2
numpy: 1.14.3

## Reflections

### Expected Bias in Data

I expected developed countries whose primary language is English to have both high percentage of articles per population 
as well as a bigger percentage of high quality articles. I expected this because developed countries would have a high
internet coverage and relatively lower populations than developing countries. Also since their primary language is English, 
it made sense to me to expect a higher quanity of articles.

### Results and Conclusions

The highest article per capita ratios came almsot solely from countries with very small populations, which was expected. SImilarly 
India and China had the lowest article per capita ratio, which was also expected due to the large populations. But apart from these two, 
the other countries were those with very small populations again like Uzbekistan, Zambia, North Korea etc. Again this could be explained
by the poor internet access in most of these countries. So the obvious question is since only English articles are being considered, is this
a fair representation because many countries have other official languages which is more accesible and used by the population.

There are numerous countries which do not have any high quality articles which was unexpected. Also, I was not able to find any of 
the countries matching my initial expectations (European and North American countries) in the top 10 lists. Berlin was a standout for 
me because I was under the impression they are quite particular about not talking in English.

Overall, due to the lack of consideration for regional languages and because the data is confined to people with active internet access,
I believe the data is very biased and thus no viable conclusions can be confidently drawn from it with respect to its reflection on the real 
world. Also the ORES API is a wild card which Ihas been trusted to give the correct quality indicators but the way AI is being programmed
for this purpose could also be having an effect. For e.g if there are more grammatical errors in an article from a non-native English speaker
is it categorized as poor? Or is the score dynamic and can be improved on edits?


## License

This assignment is released under the MIT license.

The data located on figshare is licensed under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/).

The license for population data on dropbox is unclear.

The ORES API is developed by the Wikimedia foundation and as per their site (https://blog.wikimedia.org/2015/11/30/artificial-intelligence-x-ray-specs/) the revision scores are released under a Creative Commons Zero license (https://creativecommons.org/publicdomain/zero/1.0/).
