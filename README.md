# Summary
## 1. Where in NYC are lottery retailers most found? 
-First we read in the NYS Lottery Retailer data.

-We then had to clean the data to only reflect the NYC zipcodes.

-We then added boroughs to their respective zip codes.

-From this cleaned data set, we got the count of Lottery Retailers per borough.

-Then created bar charts.

-We used the Census API to find the following fields for NYC:

    -Population
    
    -Household Income
    
    -Per Capita Income
    
    -Poverty Count
    
    -Zip Code
    
-Using this data, we calculated the Lottery Retailer Per Capita by dividing the count of retailer per borough by the population of each borough.

**This data shows that Manhattan and Staten Island have the highest Lottery Retailers Per Capita 

## 2. What is the relationship between average income and lottery sales in NYC?

-We then created the Income per Capita graph to compare to the Lottery Retailer Per Capita graph.

-We the created the Poverty Rate graph to compare to the Lottery Retailer per Capita graph.

**These charts show some correlation. The Manhattan bars are highest in both charts, but the rest of the boroughs do not correlate

## What is the relationship between poverty rate and lottery sales in NYC?

-To create graphs, we merged the cleaned Lottery data and the Census data.

-Using this data, we also found the poverty rate by dividing each poverty count by population per borough.

**These charts showed little to no correlation

## 3. What is the relationship between crime rate and lottery sales in NYC?

- An initial look at the crime dataset, which is reported by borough and precinct, shows totals for the three categories (violation, misdemeanor, and felony) fairly representative of population. Looking at crime rate per 100,000 people shows some differences based on borough.
- 
- But we wanted to look at crime versus lottery retailers on a more granular level, so we broke them down by zip code. After merging crime data with lottery retailer data, each category of crime by total incidents versus total retailers per zip code is fairly scattered and doesn’t show strong correlation. But this doesn’t account for population and is affected by a few outliers. Looking at each of the three categories of crime by retailers per 100k people and incidents per 100k people to try and account for population, it shows a little more correlation, but still affected a bit by outliers. Also the crime data was most narrowly reported by the 77 NYPD precincts which correspond to 72 zip codes. After merging with the lottery retailer-by-zip-code data, we lost some data for zip codes that had a lottery retailer, but no police precinct.

## 4. What is the relationship between graduation rates and lottery sales in NYC?

When we compare the graduation rate reports to the lottery data, we see that there isn’t a strong relationship between the number of retailers and graduation rates in their respective boroughs. Manhattan has the most retailers per capita; however, Manhattan falls in the middle ranks in terms of graduation rates. Queens and the Bronx seem to follow the logic that more lotto retailers might yield higher graduation rates; however, Brooklyn falls quite short in lotto retailers, but it does not seem to affect graduation performance. Given these results there isn’t enough evidence to conclude that a relationship exists between the the number of retailers and graduation rates. 

## 5. What is the relationship between school safety and lottery sales in NYC?

We found that there is a weak slightly positive correlation between the number of lottery retailers per capita in a zip code/borough and the average number of school crimes. We found that the average # of crimes per school in zip codes with more than 50 lottery retailers was 24% greater than zip codes with less than 15 lottery retailers. More analysis would need to be done to determine if the number of lottery retailers in a zip code is what is driving the difference in the average number of crimes per school such as control for school type and size and zip code factors such as population size and average income.

## 6. Conclusion

We failed to reject the null hypothesis. The problem was that our data on the lottery was using the metric “Number of Lottery Retailers per 100k” in each zip code. This proved problematic because the data was heavily skewed to the right and contained outliers that were from four to seven standard deviations from the mean. These zip codes were in downtown Manhattan and had very high average incomes and low populations. Our metric of “Number of Lottery Retailers per 100k” was flawed in two ways. It did not contain that actual amount of money spent on lottery tickets. It also did not take into account that tickets might be purchased in a zip code far from where someone lives, rendering invalid our school, poverty and crimes studies. The fact that our outlier zip codes were low population wealthily areas that commuters work in reinforces this idea. For further study, it would be more valuable to see actual lottery sales. (I saw online that someone had used the “Freedom of Information Act” to request this from the New York State Lottery, but had not yet received the data.) While that would be better for study, it still does not correct for the fact that commuters quite possibly purchase a large amount of lottery tickets far from their residence. The other idea was to conduct a survey about lottery purchases. The concern for this is that people might not be entirely truthful as gambling can sometimes be viewed as a taboo subject. The other concern for this would be cost.
