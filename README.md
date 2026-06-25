# A Simulated Study Of How Population Growth Affects Forest Loss in Mau Forest:Kenya
<img width="602" height="376" alt="image" src="https://github.com/user-attachments/assets/c9768259-a702-4592-832f-ab4965746b1a" />
## Main Goal
To create a mathematical model using differential equations to describe the impact of population growth on forest loss in Mau Forest,Kenya with results visualized and analyzed using R.

## Background on the Project
* I really struggled, still do, learning differential equations.
* I wanted to see how I can apply differential equations to projects since Calculus is a key Mathematical Foundation in Data Science.
* I recently did an assignment for my Sustainable Resource Management class (ENV2001) titled 'IMPACT OF POPULATION GROWTH AND HUMAN-INDUCED DEVELOPMENT ACTIVITIES ON ENVIRONMENTAL DEGRADATION:SUSTAINABLE APPROACHES AGAINST THE VICE GIVING RELEVANT EXAMPLES FROM MY COUNTRY'.
* The assignment focused on:Population growth, Human activities and Environmental degradation. 
* I became excited on combining Mathematics, Environmental Studies and Statisticss.
* This is also my first math centered project so I am very excited.

## Dataset
<img width="839" height="137" alt="image" src="https://github.com/user-attachments/assets/a8a57245-a44e-46ac-94f4-f42c35e3d072" />
* The dataset "Mau Forest" is simulated to represent population growth and forest loss in the Mau Forest.
*  I was unable to find a complete and reliable real-world dataset for this analysis hence the need to simulate it.
 
## Clean the dataset 
* Mau Forest dataset was cleaned to ensure accuracy and reliability before analysis.
* Key areas looked into were Duplicate Rows, Outliers and Missing Values.
* A total of 5000 duplicate rows were identified and removed.
* After removal, no duplicate rows remained.
* Outliers were detected using the Interquartile Range (IQR) method.
* The number of outliers identified in each column were as follows:
     * Population: 1976
     * Population Growth: 1579
     * Forest Loss: 1925
     * Agricultural Expansion: 1580
     * Settlement Expansion: 1636
* Outliers were only handled for the Forest Loss variable by winsorization because it is the dependent variable in the model, and extreme values could significantly affect the regression results.
* Other variables were left unchanged to preserve natural variation in the data.
* Missing values were found in:
     * Population: 6789
     * Forest Loss: 11229
* Missing values in each column were filled using the median value of that specific column because the dataset contained outliers and was likely skewed.
* The median is less affected by extreme values and provides a more robust estimate of the central value..
* No missing values remained in the dataset after cleaning.
<br><br>
## Multiple Linear Regression Model
  <img width="458" height="250" alt="image" src="https://github.com/user-attachments/assets/9799340c-0c9b-4acd-89f1-9311b307e229" />
* Image above is summary of the model
* A multiple linear regression model was used to examine how population growth, agricultural expansion, and settlement expansion affect forest loss in the Mau Forest.
* The model is given by:F=3329+7.213×10−6P+8.811×10−4A+1.102×10−3SF = 3329 + 7.213\times10^{-6}P + 8.811\times10^{-4}A + 1.102\times10^{-3}SF=3329+7.213×10−6P+8.811×10−4A+1.102×10−3S
* Where:
  * F = Forest Loss
  * P = Population
  * A = Agricultural Expansion
  * S = Settlement Expansion
* Population has a statistically significant but very small effect on forest loss
* Agricultural expansion and settlement expansion are not statistically
  significant in this model.
* The model has a very low R^2, meaning it explains very little variation in forest loss
* This suggests that forest loss is influenced by other factors not included in the model
<br><br>
## Differential Equations
* Differential Equations was  used to represent forest loss as a dynamic process changing over time showing how changes in human activities influence the rate of forest depletion..
* The model was written as:
dFdt=7.213×10−6P+8.811×10−4A+1.102×10−3S\frac{dF}{dt} =
7.213\times10^{-6}P +
8.811\times10^{-4}A +
1.102\times10^{-3}SdtdF​=7.213×10−6P+8.811×10−4A+1.102×10−3S
* dFdt\frac{dF}{dt}dtdF​ represents the rate of change of forest loss over time
The equation shows that forest loss changes depending on population, agricultural expansion, and settlement growth
* Assuming the variables remain constant:
dFdt=k\frac{dF}{dt} = kdtdF​=k
* Integrating gives:
F(t)=kt+CF(t) = kt + CF(t)=kt+C
* Where C represents the initial forest condition
  <br><br>
## Visualizations
### 1.Population vs Forest Loss (Scatter Plot)
<img width="480" height="480" alt="population_vs_forest_loss" src="https://github.com/user-attachments/assets/d3d24341-fd3f-467b-9dcb-5cd1008bbaf0" />
* This scatter plot shows the relationship between population and forest loss in the Mau Forest.
* Each point represents a combination of population size and forest loss.
* The purple points show a wide spread, indicating high variability.
* The green line represents the line of best fit (regression line).
<br>
#### Interpretation of Population vs Forest Loss (Scatter Plot)
* The points are widely scattered with no clear pattern.
* The regression line is almost flat, showing very little change in forest loss as population increases
* This suggests that population has a very weak relationship with forest loss
<br>
#### Conclusion
* The graph indicates that population growth alone does not strongly explain forest loss in the Mau Forest, as there is no clear trend between the two variables.
  <br><br>
### 2.Forest Loss Over Time (Time Series Plot)
<img width="480" height="480" alt="forest_loss_over_time" src="https://github.com/user-attachments/assets/0f420123-6394-4711-8eb1-3f43a721c56c" />
* This graph shows how forest loss changes over time in the Mau Forest.
* The x-axis represents years.
* The y-axis represents forest loss (in hectares).
* The green line connects forest loss values across different years.
<br>
#### Interpretation
* The graph appears very dense because of many overlapping data points.
* There is no clear upward or downward trend visible.
* Forest loss values vary widely over time
<br>
#### Conclusion
* Forest loss does not show a clear consistent trend over the years, indicating that changes in forest loss are irregular and influenced by multiple factors.
  <br><br>
### 3. Agriculture vs Forest Loss (Scatter Plot)
<img width="480" height="480" alt="agricultural_expansion_vs_forest_loss" src="https://github.com/user-attachments/assets/576cd760-d219-48a7-9475-fd2b2f3a4fe2" />
* This scatter plot shows the relationship between agricultural expansion and forest loss.
* Each red point represents a combination of Agricultural expansion and Forest loss.
* The points are widely spread across the graph
<br>
#### Interpretation
* There is no clear linear pattern between agricultural expansion and forest loss
* The data is highly scattered, indicating weak or inconsistent relationship
<br>
#### Conclusion
* The graph suggests that agricultural expansion alone does not strongly explain forest loss in the Mau Forest.

