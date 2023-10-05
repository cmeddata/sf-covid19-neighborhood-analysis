# Assessing COVID-19 in San Francisco: A closer look at Neighborhoods and its impact on COVID-19 cases

## Background : 

The COVID-19 pandemic has profoundly affected communities worldwide, with each region facing unique challenges in the battle against the virus. As we strive to better understand the spread of COVID-19, its impact on public health, and the factors that contribute to its transmission, a closer examination at the neighborhood level becomes increasingly important.

San Francisco, known for its diverse neighborhoods and vibrant communities, presents a compelling case study for assessing the impact of COVID-19. While the city has implemented various measures to mitigate the spread of the virus, such as social distancing, mask mandates, and vaccination campaigns, the distribution of COVID-19 cases within different neighborhoods may vary significantly.

This research project aims to delve into the intricate relationship between San Francisco's neighborhoods and the cumulative rate of confirmed COVID-19 cases. By focusing on a range of variables, including geographic coordinates (longitude and latitude), area (measured in Square Feet and Square Miles), poverty rates, and demographic composition (Asian %, Black %, White %, Hispanic %, Other %), we seek to uncover patterns and disparities that shed light on how different neighborhoods have been affected by the pandemic.

## Key questions that will guide our investigation include:

 - **Geographic Influence**: Are certain neighborhoods more susceptible to COVID-19 cases based on their geographic location within the city? Does longitude play a significant role in the spread of the virus?

 - **Socioeconomic Factors**: How does poverty rate within a neighborhood correlate with the cumulative rate of COVID-19 cases? Are economically disadvantaged neighborhoods experiencing a higher burden of infection?
   
 - **Demographic Variation**: Do neighborhoods with varying demographic compositions exhibit different rates of COVID-19 cases? Are certain ethnic or racial groups disproportionately affected?

## Hypothesis

Neighborhood characteristics, including factors such as poverty rates, geographical location (latitude, longitude, square feet and square miles), and race/ethnicity, have an influence on COVID-19 rates in San Francisco. 

## Methodology

 - **Data Collection**: We obtained COVID-19 datasets for San Francisco neighborhoods, initially from DataSF, which included cumulative case rates and geographic coordinates. To enhance our analysis, we supplemented this with additional data from The San Francisco Standard, offering insights into poverty rates and ethnic demographics, sourced from the U.S. Census.

 - **Data Filtering**: We imported and meticulously filtered the data, retaining only the relevant information for our study. Our data set contains various information on 36 different neighborhoods in San Francisco. We used the rate of cumulative confirmed cases in each area, per 10,000 residents, calculated as (count/acs_population)*10000, as our dependent variable. Population, cumulative confirmed cases, longitude, latitude, square miles, square feet, and ethnicity (categorized as asian, black, white, hispanic, and others) are our explanatory variables.

 - **Regression Analysis**: Utilizing Excel's Data Analysis ToolPak, we applied Multiple Linear Regression to our dataset, enabling the calculation of regression statistics and ANOVA.

 - **Descriptive Statistics**: We conducted descriptive statistical analysis on our dataset, extracting key metrics such as mean, median, standard deviation, and other relevant measures.

 - **Correlation Assessment**: A correlation matrix was generated to assess potential correlations among variables that could influence our data analysis outcomes.

## Analysis Summary

 - **MULTIPLE R**: The multiple R value, which is 0.9245 in this case, represents the correlation between the dependent variable (rate_of_cumulative_confirmed_cases) and all the independent variables (cumulative_confirmed_cases, longitude, latitude, Square_Miles, Poverty rate %, Asian %, Black %, White %, Hispanic %, and Other %). It indicates a strong positive linear relationship between the variables.

 - **R SQUARE (R²)**: The R-square value, which is 0.888, measures the goodness of fit of the regression model. It represents the proportion of the variance in the dependent variable that is explained by the independent variables. In this case, approximately 84.51% of the variance in the rate_of_cumulative_confirmed_cases can be explained by the independent variables in the model.

 - **ANOVA (Analysis of Variance)**: The ANOVA table summarizes the overall statistical significance of the regression model. It compares the variance explained by the regression model (Regression) with the unexplained variance (Residual). The F-statistic is used to test whether the regression model is significant. In this case, the F-statistic is 15.76, and the associated p-value (2.03E-08) is very close to zero, indicating that the model is statistically significant.

 - **STATISTICALLY SIGNIFICANT VARIABLES (P <0.05)**: The results show that the statistically significant variables are “population”, “cumulative confirmed cases” and “longitude”.

 - **NON-SIGNIFICANT VARIABLES (P>0.05)**: The results also show that the not statistically significant variables are the latitude, square miles, square feet, poverty rate, and ethnicity (Asian %, Black %, White %, Hispanic %, and Other %)

## Correlation Matrix:

- **Population and cumulative confirmed cases**: A strong positive correlation was observed between population and cumulative confirmed cases, indicating that areas with larger populations tend to have higher numbers of confirmed cases. This insight highlights the significant impact of population density on the spread of the condition. We chose to remove population because the rate is calculated per 10 000 people, making population less statistically significant than the confirmed cases.

- **Square Feet and Square Miles**: Square feet has been removed from the analysis as it is a unit of measurement more suited for smaller areas like buildings. Square miles, being a more appropriate metric for larger geographical areas, will better serve our analysis.

- **Hispanic % and Other % **: Since they are highly correlated with no obvious motive to remove one or the other, we compared the correlation of each predictor with the dependent variable, and removed the one with the weaker correlation. Thus, percentage of residents that identify as Other has been removed as a predictor, with a correlation of 0.451 compared to 0.566.

## Rate of Cumulative cases V.S. Poverty Rate:

![Rate_VS_Poverty](https://github.com/cmeddata/sf-covid19-neighborhood-analysis/assets/124543750/11d2d1ff-68d7-4232-889b-ce4d2d51a0b7)

# Key Insights:

 - **Poverty Rate's Impact**: The poverty rate, defined as the percentage of households below the poverty line in each neighborhood, emerges as a pivotal factor influencing the rate of cumulative COVID-19 cases.
   
 - **Magnitude of Impact**: The coefficients represent the estimated change in the rate of cumulative confirmed cases for a 1-unit increase in each respective variable, assuming all others are held constant. With a coefficient of -1888.3778, the data suggests that higher poverty rates are associated with an increased rate of cumulative COVID-19 cases.

 - **Significance**: The significance of this relationship underscores the importance of socio-economic factors in understanding the spread of the virus.

 - **Neighborhoods most affected**: Based on our dataset and analysis, the neighborhoods most affected by this are Chinatown with a 32.9% poverty rate, Tenderloin with 26.5%, Western addition with 19.6% and Japantown with 19%.

 - **Neighborhoods least affected**: With some the lowest poverty rates in the city, Presidio (0.19% Poverty rate), Seacliff (0.28% Poverty Rate), Marina (0.41% Poverty Rate) and Noe Valley (0.42% Poverty Rate) are least affected by this.

This analysis not only underscores the critical role of poverty rates in influencing COVID-19 transmission rates but also emphasizes the need for targeted interventions in neighborhoods with higher poverty rates. Further research and public health initiatives may be required to address this disparity and mitigate the impact of the pandemic on vulnerable communities.

# Conclusion
 - The analysis reveals a crucial relationship between poverty rates and the rate of cumulative COVID-19 cases, a key metric for measuring the pandemic's spread. This relationship is supported by a statistically significant p-value of 0.0445384, indicating significance at the 0.05 level

## Cumulative Rate V.S. Geographical Statistics

![Rate_VS_Longitude](https://github.com/cmeddata/sf-covid19-neighborhood-analysis/assets/124543750/9d41f35f-8740-49cf-94b9-ee14765b30fe)

# Key Insights

- **Geographical Statistics Impact**: The geographical statistics (Longitude, Latitude, Square miles and Square feet) have some factors that have significant impact and some that don’t. Specifically, we have very strong evidence that the longitude significantly impacts the rate, as its p-value of 0.0000931 is very close to zero. The rest however have a p-value which means that they are non-significant to the cumulative rate of covid-19.

- **Significance**: From the graph we can see that the cumulative rate decreases the higher you go in the peninsula. This may be attributed to neighborhoods with lower poverty rate being higher while neighborhoods with higher poverty rate are lower in the peninsula.

- **Neighborhoods most affected**: The neighborhoods most affected by this data are Mission Bay, Financial District and Bayview Hunters Point being the lowest areas longitude wise in the peninsula while also boasting some of the highest cumulative covid-19 rates in the city.

- **Neighborhoods least affected**: The neighborhoods least affected by this are Outer Richmond, Lakeshore, and Seacliff. These neighborhoods are the neighborhoods with the highest longitude in the peninsula while also maintaining some of the lowest poverty rate in the city.This analysis shows that the geographical statistics of your neighborhood mostly do not have an effect on the transmission of COVID-19 except for the latitude. The latitude of the neighborhood mostly correlates to the poverty rate as seen by the graph, the closer you get to the areas with higher poverty rate, the higher the cumulative rate gets while the closer you get to the neighborhoods with the highest latitude in peninsula which are also some of the neighborhoods with the lowest poverty rate in the city, the lower the cumulative rate gets.

This analysis shows that the geographical statistics of your neighborhood mostly do not have an effect on the transmission of COVID-19 except for the latitude. The latitude of the neighborhood mostly correlates to the poverty rate as seen by the graph, the closer you get to the areas with higher poverty rate, the higher the cumulative rate gets while the closer you get to the neighborhoods with the highest latitude in peninsula which are also some of the neighborhoods with the lowest poverty rate in the city, the lower the cumulative rate gets.


## Cumulative rate of confirmed cases V.S. Cumulative confirmed cases

# Key Insights

 - **Cumulative Confirmed Cases Impact**: The cumulative confirmed cases while being directly proportional to the cumulative rate has no significant impact on it. With a P-Value of 0.0798749 which is above 0.5 this metric has no significant impact on our cumulative rate.

 - **Neighborhoods with Most Confirmed Cases**: The neighborhoods with the most cumulative confirmed cases are Mission with 15,268 confirmed cases, Bayview Hunters Point with 15,055 cases while also having the highest rate of cumulative cases at 3912.42, and Sunset/Parkside with 14,048.

 - **Neighborhoods with the least confirmed Cases**: The neighborhood with the least confirmed cases was Seacliff with 365 cases.

This analysis shows that the cumulative confirmed cases is the accumulated number of cases in the area, up until the last collection date of September 24th, 2023. From our dataset, we see that the average cumulative confirmed cases in San Francisco is 9954.3243. The smallest amount of cumulative confirmed was in Seacliff with 365 cases, and the maximum is 15,268 cumulative confirmed cases in Mission. While the cumulative number of cases is statistically insignificant for what we are trying to answer, it is still important to note that it is still directly proportional with the cumulative rate.

## Cumulative rate of confirmed cases V.S. Rate of Ethnicity

# Key Findings

 - We also collected data on the rates of ethnicities in San Francisco, categorized as Asian, Black, White, Hispanic and Other. However, after fitting a multiple linear regression and checking for multicollinearity, none of these were statistically significant, which meant that ethnicity did not have an impact on the rate of cumulative confirmed cases.

 - The COVID-19 pandemic has posed unique challenges to communities worldwide, necessitating a comprehensive understanding of its impact and contributing factors. In this research project, we focused on San Francisco's neighborhoods to investigate the relationship between various variables and the cumulative rate of confirmed COVID-19 cases.


## Summary Of Key Findings And Insights:

# Poverty Rate's Influence:

- Poverty rate % emerged as a significant and influential factor in the rate of cumulative COVID-19 cases.
- Higher poverty rates were associated with an increased rate of cumulative COVID-19 cases.
- Neighborhoods with the highest poverty rates, such as Chinatown and Tenderloin, experienced the most significant impact.


# Geographic Factors:

 - Geographic factors, including longitude and latitude, exhibited varying impacts on the cumulative rate.
 - Longitude was a statistically significant variable, indicating that neighborhoods' positions within the city played a role in COVID-19 transmission.
 - Cumulative rates tended to decrease as neighborhoods moved northward on the peninsula, possibly due to variations in poverty rates.

# Ethnicity and Demographics:

- Ethnicity (Asian %, Black %, White %, Hispanic %, and Other %) did not show statistically significant correlations with the cumulative rate of COVID-19 cases.
- This suggests that ethnicity itself had little to no impact on the likelihood of contracting COVID-19 in San Francisco.


## Final Conclusion

This research project provides valuable insights into the complex relationship between neighborhood characteristics and the spread of COVID-19 in San Francisco. Key takeaways include the significant influence of poverty rates on COVID-19 transmission, the role of longitude in geographic disparities, and the limited impact of ethnicity on infection rates.

Our findings highlight the importance of addressing socio-economic disparities in public health interventions. Targeted efforts should focus on neighborhoods with higher poverty rates to reduce vulnerability to COVID-19. Geographic considerations should also inform localized strategies.

Furthermore, this research underscores the need for ongoing monitoring and analysis of COVID-19 data to adapt public health responses effectively. It also serves as a reminder that pandemics impact communities differently and that tailored interventions are crucial for addressing the unique challenges faced by each neighborhood.



## License

This project is licensed under the MIT License - see the LICENSE.txt file for details.



  

 



