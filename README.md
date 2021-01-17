## WorldHappinessReport

### Data Source:
Each year since 2012, the United Nations publishes a World Happiness Report detailing changes in perception of happiness across the countries. The data for these reports is taken from data collected by Gallop World Poll, World Health Organization, and World Bank. This Happiness score is an average of national responses based upon self-perceived happiness. The datasets for our analysis were open sourced and downloaded from https://www.kaggle.com/mathurinache/world-happiness-report.  
 We tried to extract the relationship of factors GDP, freedom to make life choices, family support, and healthy life expectancy with happiness of nations. We hypothesized that mentioned factors increase the happiness of nations. 
### Regression Analysis:

### Model  Assumptions:
#### (Linearity /Residuals are normal/Check for Homoscedasticity)
We choose Linear Regression as a predictive Modelling Technique as our response variable is continuous. For Linear Regression we checked a few assumptions so that we can apply Linear regression. First assumption of linearity of predictors with target variables was checked using scatterplots. Variables Trust and Generosity did not show linear relation with target. Second assumption is Residuals are normal. We used residuals instead of the predictors on the y-axis so that we could check for linearity without worrying about other possible violations like collinearity between the predictors. The residual plot reveals that for Economy, Health, Family and Freedom residuals were randomly scattered with no clear pattern. But variables Trust and Generosity were not randomly scattered hence violating the conditions of residuals normality. We performed sqrt transformation to make them linear with target but even after transformation they show little correlation with response.
### Feature Selection: 
We selected our features Economy, Health, Family, and Freedom for our linear model based on our following observations.  Although Trust and Generosity had normal distribution after sqr-transformation but heatmap displayed less correlation with Score. Features were tested using Forward Stepwise LR. Adjusted R-square was 0.616 with a single predictor Economy. R-square adjusted increased with addition of Freedom predictor (0.708). Adjusted R-square further increased with the addition of Freedom and Health predictors to 0.734 and 0.748, respectively. We observed a stepwise decrease in RMSE values from 0.7190 to 0.56942 after adding four predictors. 
### Model Building ###
We built a regression model and estimated the coefficients through OLS. Interpretation of p-value, p-value for each of the predictor Economy, Family, Freedom and health is less than significance level (0.5) so we can say that they are predictors for our response variable. The R2 and adj. R2 were 0.749 and 0.748, respectively (Figure-2). The largest regression coefficient for Freedom of 1.9173 means that on average, every 1 unit increase in Freedom (to make choices) is associated with an average increase of 1.158 in Score. The greater the freedom for people to make their own choices, the greater the happiness. 
Another significant feature, indicated by a high regression coefficient, is Economy of 1.1833. This means that on average, each point increase in Economy is associated with an increase of 1.11 in happiness score. Any country’s good Economy or GDP per capita leads to general happiness. Our third most significant feature is Health (0.9901). This means that on average, each unit increase in Healthy life expectancy is associated with an increase of happiness score. Our fourth most significant feature Family is indicated by a high regression coefficient of 0.5687.
### Model evaluation:
Residual plot and Q-Q plot. We created residual versus fitted values. A perfect model would give a scatterplot where all the data lies on the 45 degree line. That would mean that x = y, and every predicted Score would have equaled the actual score. The data does not show any pattern between fitted values and residuals; no assumptions have been violated. Model RMSE:  0.5792 and MSE:  0.335509 Lower RMSE indicates a better fit. Our q-q plot is also showing a straight line, with some points upper and lower end are not normal.

### Conclusion:
With the Linear Regression model we proved that 4 variables Economy, Family , Health and Freedom leads to happiness.   The coefficient of determination or r-squared, tells us that 75% of the total variance in the Score can be explained by the linear regression model. This is an important statistic that measures how 'good' our model is at predicting Score. 

