# wine_and_climate_change

Our Current Research Questions:
## Is there a correlation between rising temperatures and its effect on wine production?
Hypothesis: There is a statistically significant correlation between rising temperatures and wine production.
Null: There is no statistically significant correlation between rising temperatures and wine production.
## Is there a correlation between rising temperatures and the creation of new wine industries in regions previously unfit for wine production?
Hypothesis: There is a statistically significant correlation between rising temperatures and new wine industries.
Null: There is no statistically significant correlation between rising temperatures and the creation of new wine industries.
## Which geographical regions can expect to see an increase in wine production and which regions can expect to see a decrease in wine production given the expected rise in temperature?
Hypothesis: There is statistically significant difference in the expected change in wine production between geographical regions as a result of the expected rise in temperature.
We expect to see geographical regions traditionally too cold to grow wine to see an increase in production due to rising temperatures, and those traditionally ideal to see a decrease in wine production.
Null: There is no statistically significant difference in the expected change in wine production between geographical regions as a result of the expected rise in temperature.



CSV Order: 
1. GlobalLandTemperatures_GlobalLandTemperaturesByCountry.csv
2. global_temps.csv
3. wine-production.csv
4. merge_data.csv
5. country_data_df.csv

Project Analysis
## Does climate change affect global wine production?

## Is there a correlation between rising temperatures and its effect on wine production?
We analyzed over 100 countries to determine if a correlation exists between rising temperatures and wine production. While we did see weak to moderate correlation in some countries, overall we determined that a statistically significant correlation across all countries cannot be concluded with our current data sets. 

Greece is an example where we see a weak to moderate correlation, with an r-value of -.5. As temperatures have increased, especially over the last decade, wine production has decreased. 

South Africa is an example where we see a weak correlation, with an r-value of .39. Temperatures here have fluctuated, but overtime have not increased or decreased significantly. However, wine production has been increasing consistently since 1980. This indicates that there are other factors as play influencing wine production.

## Is there a correlation between rising temperatures and the creation of new wine industries in regions previously unfit for wine production?
In my group's discussion on how climate change may affect wine production, an interesting question arose: how might the gradual increase in global temperatures positively influence the wine industry? Surely there must be some regions whose temperatures have changed, and can now grow grapes more efficiently. Finding this topic interesting, I took it upon myself to search for a correlation.

The core of my analysis focused on the comparison between increases in wine production by country and the respective changes in their average temperature. This comparison aimed to discern any patterns or correlations between these two variables. Given the limited nature of our data, I determined that the best way to find this correlation would be to look at countries whose wine production has seen significant growth in recent years. Arbitrarily, I chose 1990 as a start year, knowing that 1961 was the oldest year in our data set. In hindsight, this was a poor decision, as not every country had wine production data that went back to 1961. China, for example, has data that goes back only as far as 1981. Thus, it appears as an outlier in the dataset, as it does not have enough historical data to offset its recent growth. 

Another massive oversight on my part was assuming that our wine data extended to 2023. If you look at my code, there is a variable ‘recent_period_start’ which subtracts 33 from from the most recent year in our dataset in an attempt to establish the year where I wanted to start tracking recent market growth. But our dataset only extended to 2020, which meant that the ‘recent_period_start’ variable actually begins in 1987, not 1990. This was a very sloppy mistake on my end. 

Before knowing that my market growth data was flawed, I knew that the results would be irrelevant due to the limited nature of our data. While correlations might have existed, causation could not be determined. Thus, in presenting my data, I aimed to show 1 case study which indicated a correlation, and one that did not. There were several countries that showed statistical significance and correlation across the board, but since they were all essentially inconclusive,  I figured one demonstration would suffice. 

To acquire the data I needed, I started by creating a table that calculated the growth rates for all countries, and sorted them in descending order. From this table, I generated a bar graph to show the growth rates of each country. 

I then created another table that returned all statistically significant countries (with an r-value threshold of .3) for Wine Production over Time, Wine Production & Average Temperature, and Average Temperature over Time. I also cleaned the data for countries whose p-values were <0.05. 

Once the data collection was completed, I was able to generate graphs from our interactive charts in Python. I chose to show the data for New Zealand, because it was an example of a country that failed to correlate, and Japan, because it was the highest correlation for wine production & average temperature such that the higher the temperature, the more wine produced.

New Zealand experienced the highest rate of wine production growth of all the countries within our dataset (outside of China, of course). Since 1987 (originally meant to be 1990), their wine production has increased by 321.16%. In addition to this increase, New Zealand has also experienced a relatively weak (r=0.3719) positive trend in average yearly temperature, confirming a rise in temperature since 1961. However, when wine production is correlated to average temperature, there is a statistically insignificant correlation (r=0.2972), such that higher temperatures did not correlate with more wine production. Based on the limited parameters of our analysis, then, we can confirm that the wine production growth in New Zealand is not related to higher temperatures.

Japan, on the other hand, does show statistically significant correlations for each of the metrics. It experienced a 208.79% increase in wine production from 1987, Its temperature over time correlation was positive and moderately correlated (r=0.5401), and most importantly, wine production was positively correlated to higher average temperatures. Knowing this, we can say that there is a correlation between higher temperatures and the growth in Japan’s wine industry. But we cannot say that higher temperatures were the cause of wine production growth in Japan. 

Conclusion
In conclusion, the answer to whether higher temperatures created new wine industries is inconclusive. While I was able to find some correlations, those correlations are far from telling the entire story. As Dwight pointed out during one of our project discussions, the topic we chose requires a plethora of data sets, and it could take years to clearly demonstrate a statistical relationship between a rise in temperature and a growth in wine production.

Discussion
There were many illogical decisions made towards the beginning of the project that only occurred to me when it was unfortunately too late. I found that as I worked through the project, many of my initial decisions made less and less sense. The more I came to understand the process of statistical analysis through actual practice, the more I realized how ignorant I was at the beginning. I think that if I had more time, I would have been able to course correct. But given the short time frame, I had to march forward without a solid understanding, and it unfortunately led me to a lot of problematic decisions. 

If I had more time, I would have pulled more data sets to help paint a more accurate picture. As Mustafa pointed out in his section, things like soil type, government investment into industry, or even availability to water can all have a significant impact on how the data gets interpreted. And, in general, more time would have allowed for a lot more trouble shooting and course correction, which would in turn have resulted in better results. 

## Which geographical regions can expect to see an increase in wine production and which regions can expect to see a decrease in wine production given the expected rise in temperature?
The analysis found that while some countries showed weak to moderate correlations between temperature and wine production, overall there was not a statistically significant correlation across all countries with the current data sets.

A few key points:
The analysis looked at New Zealand as a case study. While New Zealand had the highest rate of wine production growth and experienced a weak positive trend in average yearly temperature, there was no statistically significant correlation between higher temperatures and increased wine production.
Japan was another case study that did show statistically significant correlations between increased temperatures and growth in the wine industry. However, causation could not be established.
The author acknowledged several limitations and flaws in the analysis, including limited data sets, poor choice of start year for analysis, and incorrect assumptions about the time period covered by the wine production data.
The author concluded that more data sets and time would be needed to clearly demonstrate a statistical relationship between temperature rise and growth in wine production in different regions.

In summary, while the initial hypothesis was that colder regions may see an increase in wine production and traditionally ideal regions may see a decrease, the limited analysis conducted was not able to confirm this or make clear predictions for specific geographical regions. More comprehensive data and further study would be required to answer the question posed.
