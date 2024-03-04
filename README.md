This repository evaulates the trends in the Netflix Top 10 dataset. 

Attached is that dataset downloaded January 11 2024 in both CSV and Excel format. 

The IPYNB file labeled litreview includes an outline of the data, univariate analysis (histograms) and bivariate analysis (scatterplots) of the unaltered data. 

Also attached is the PDF and IPYNB file of the Inital Code and Results which includes the same content as the ipynb litreview file in additon to the following code and results explained below.

We first look to see whether date correlates with shows that have larger cumulative weeks in Top 10? Firstly, we find the average cumulative weeks in Top 10 by month and plot this in a histogram. We can see the data is non-normally distributed amongst the months which means we must use non-parametric statistical testing to determine the relationship between month and cumulative weeks. Secondly, we perform t-test between each month pairing. Although the data is non-normal, we assume the dataset is sufficiently large. 

We then look at whether shows in the US are more likely to make the top 10 in other countries and in which countries. Firstly, we look at a list of every country in our dataset. We subset the data for shows that make the Top 10 in the US and then count the frequency which these shows make the top 10. We isolate the top 10 most common shows/movies that make the Top 10. For reference, we can see the top 10 that make the Top 10 in Canada are different than the US. We then count the number of times the top 10 Top 10 US shows/movies make the Top 10 in other countries and store this in a table with the 10 show/movie names and the counts of the number of times that show/movie made the Top 10 in every other country. We perform statistical analysis for every country in relation to the US to see which countries may affect or resemble US top 10. We attempt to determine the percentage of statistically significant countries that are english speaking, however, it is complex to determine the definition of english-speaking country, and to compile a list of all such countries. Thus, this section of code can be ignored for the sake of our analysis. Lastly, we can perform decision tree classification given the nature of our dataset to see whether we can accurately predict Top 10 media in a country, given that we know which media makes the top 10 in said country and the US. We perform this for both Canada and Argentina to assess whether we can accurately predict Top 10 shows/movies given US shows and movies. The decision tree, it's confusion matrix, and the statistics from the classification report are printed out.

We also look at whether shows with more seasons make the top 10 list more often. We start by isolating the season_title number from the season_title column which proved complex due to varying formatting styles. We eliminated many rows in which formatting varied and despite errors, made the assumption that season number was after the word Season. We then selected for only seasons 1 through 10 (in attempt to eliminate rows where season_number was extracted incorrectly). We then found the average cumulative weeks in Top 10 for each season and plotted this to visualize potential linear trends and whether shows with more seasons stay in the Top 10 list for longer. We also plotted the distribution of season number and frequency in Top 10 to determine whether shows with higher seasons more frequently appear in the Top 10. 

Our final analysis investigated whether TV shows or movies spent more time on the cumulative weeks in Top 10 as per our preliminary analysis showing that TV shows made the Top 10 for up to 60 weeks, where movies only made the top 10 for up to 40 weeks. We compared the histograms of both TV shows and movies and then calculated the average cumulative weeks in top 10 for each cateogry and ran statistical analysis. 
