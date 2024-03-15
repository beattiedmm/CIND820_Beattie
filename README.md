This repository evaulates the trends in the Netflix Top 10 dataset. 

Attached is that dataset downloaded January 11 2024 in both CSV and Excel format. 

The IPYNB file labeled litreview includes an outline of the data, univariate analysis (histograms) and bivariate analysis (scatterplots) of the unaltered data. 

Also attached is the PDF of the Inital Code and Results and the IPYNB file of all code named 'CIND820_NetflixTop10_Country.ipynb' which includes the same content as the ipynb litreview file in additon to the following code and results explained below. Many algorithms were completed, one for each respective research question with the exception of predicting Top 10 trends among countries in which chi-square analysis and decision tree classification were performed.

We first look to see whether date correlates with shows that have larger cumulative weeks in Top 10? Firstly, we find the average cumulative weeks in Top 10 by month and plot this in a histogram. We can see the data is non-normally distributed amongst the months which means we must use non-parametric statistical testing to determine the relationship between month and cumulative weeks. Secondly, we perform t-test between each month pairing. Although the data is non-normal, we assume the dataset is sufficiently large. We can see that some months have statistical differences (February and December) and some months do not (January and February). 

We then look at whether shows in the US are more likely to make the top 10 in other countries and in which countries. Firstly, we look at a list of every country in our dataset. We subset the data for shows that make the Top 10 in the US and then count the frequency which these shows make the top 10. We isolate the top 10 most common shows/movies that make the Top 10. For comparison, we can see the top 10 that make the Top 10 in Canada are different than the US. We then count the number of times the top 10 Top 10 US shows/movies make the Top 10 in other countries and store this in a table with the 10 show/movie names and the counts of the number of times that show/movie made the Top 10 in every other country. We perform statistical analysis for every country in relation to the US to see which countries may affect or resemble US top 10. We attempt to determine the percentage of statistically significant countries that are english speaking, however, it is complex to determine the definition of english-speaking country, and to compile a list of all such countries. Thus, this section of code can be ignored for the sake of our analysis. Lastly, we can split the dataset into train and test set and perform decision tree classification to see whether we can accurately predict Top 10 media in a country, given that we know which media makes the top 10 in said country and the US. We perform this for both Canada and Argentina to assess whether we can accurately predict Top 10 shows/movies given US shows and movies. The decision tree, it's confusion matrix, and the statistics from the classification report are printed out. The accuracy of the decison tree to predict Canadian Top 10 is 69% whereas the accuracy for Argentina predictions is slightly smaller at 63%. This is not a large difference, but future studies could compute the accuracy of decision trees for other countries to see if any trend is noticed. In our study, we will  note that the accuracy is slightly higher in Canada, an english speaking country, comapred to Argentina, a non-english speaking country. Interstingly, precision and recall for positve values (is in country top 10, value = 1) for Canada is larger than precision and recall for negative values (not in country top 10). Differingly, we see that precision and recall for negative values is higher than for positive values for Argentina data predictions. In addition to country comparison, the Canada decision tree predictions were completed a second time with a different random state value where 5-fold cross validation was completed. This was to test whether a model would perform better if trained on a different subset of the data. The accuracy, precision, and recall values were slightly lower in this model but accuracy (67%) was still higher than Argentina prediction accuracy. The cross validation scores are .72916667, 0.70833333, 0.68229167, 0.734375, 0.671875 with an average of 0.7052083333333333.

We also look at whether shows with more seasons make the top 10 list more often. We start by isolating the season_title number from the season_title column which proved complex due to varying formatting styles. We eliminated many rows in which formatting varied and despite errors, made the assumption that season number was after the word Season. We then selected for only seasons 1 through 10 (in attempt to eliminate rows where season_number was extracted incorrectly). We then found the average cumulative weeks in Top 10 for each season and plotted this to visualize potential linear trends and whether shows with more seasons stay in the Top 10 list for longer. We can also analyse Pearson correlation which shows that there is no linear relationship between season number and how long a show stays in the top 10. We also plotted the distribution of season number and frequency in Top 10 to determine whether shows with higher seasons more frequently appear in the Top 10, which also does not appear to be the case. We did not compute statistical analysis for this as the histogram shows season 1 makes the top 10 the most frequently and frequency dwindles the higher the season number. 

Our final analysis investigated whether TV shows or movies spent more time on the cumulative weeks in Top 10 as per our preliminary analysis showing that TV shows made the Top 10 for up to 60 weeks, where movies only made the top 10 for up to 40 weeks. We looked at the histograms of both TV shows and movies and then calculated the average cumulative weeks in top 10 for each cateogry and ran statistical analysis. Wilcoxon Rank Sum test says the difference in averages, 4.9 and 2.0, is statistically significant. 

Overall, we can conclude that histograms are a strong tool to visualize trends in data and statisical analysis can help determind the significance of the trends. We can also see that decision tree classification can be used to predict top 10 media in other countries, however, accuracy is sufficient but not great.



Please note that this GitHub will remain the most recent version of code/results. There is a pdf error on the assignment page of D2L, however, the code uploaded on D2L, is the same as the code found here in GitHub. The results labeled final are currently works in progress updated as I complete the final report, which I have made some changes to compared to the initial code/results.

The final results include a histogram of January month frequency distribution for cumulative weeks in top 10 showing non-normal distribution for data entries of the month January. 
