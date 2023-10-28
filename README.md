## Comparing Education Quality with Chess Players

### Motivation:

I have a Bachelor’s degree in Psychology and one of the most interesting series of studies I learned about was ones looking at chess Grandmasters for memory retention, expertise studies, and similar topics. I’m interested in the popular perception of good chess players as being more highly intelligent, and seeing if that idea holds up compared to the data.

### Questions:  

•	What’s the breakdown of chess players by country?
•	What’s the breakdown of chess player ranks by country? 
•	Is there a correlation between education quality and having more chess players?
•	Is there a correlation between education quality and having more highly ranked chess players?
•	Is there a stronger correlation between chess players than education, such as GDP or population?

### Process and Normalization:

I pulled several csvs from my sources. Looking at the data, I did some minor cleaning on the FIDE players, then pulled the world education ranks intending to merge them. The world education ranks weren't abbreviated, so I found a list of the official country abbreviations as well. Upon attempting to merge them I discovered the FIDE Federations don't use the official 3-letter country abbreviations, so about half of the countries I had to go through and manually assign abbreviations. After this, I aggregated tables based on a given country, listed both the total players for a given federation and divvied them up into their ranks so that I could look at players of a specific rank or higher later. I did some exploratory visualizations at this point to understand what I was looking at. After doing more data cleaning, I ran the numbers and got my initial correlations and results.

At this point I'm wondering if my results are being thrown off by being forced to use Pearson's to compare a rank and a number. I pulled in Spearman's Rank correlation and converted my non-rank variables to ranks to see if that changes anything. I start getting more legible charts and the pvalues rise, so that's a plus.

Next, I pulled in some economic factors to see if there was a more relevant variable I was missing. I wasn't able to go deep on this but the numbers but the correlations I get for GDP and GDP per Capita are pretty weak, so I decide to stay the course and not focus on those new factors.

After that, all that remained was visualizing the data and trimming it down to the appropriate length.

### Data Sources and Technologies:

FIDE: the International Chess Federation.
Worldtop20.org: education quality rating website.
Worldpopulationreview.com: country GDP and population data.
Iban.com: official country abbreviations list.
https://en.wikipedia.org/wiki/Chess_rating_system: Where I pulled the ranking categories themselves from.

Python: database merging, data cleaning, correlations, miscellaneous stuff.
Tableau: interactive dashboards.

### Conclusions, and Next Steps:

I found that while there is a weak correlation between education quality and number of chess players, its a weak correlation. When looking exclusively at higher ranked players, the correlation gets weaker. GDP and population correlations were also found to be weak. Most countries of any education rank don't have that many more ranked chess players than ones down the list.

For follow-up studies I would suggest looking at outlier countries based on education and population, such as Iceland and India and seeing what's there.

Alternatively, it would be interesting to compare a country's total number of physical sport players, such as soccer/football, in order to control for countries whose lack of access to resources don't allow for a signifcant number of people to spend their lives dedicated to playing a game.