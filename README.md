# Introduction
The dataset contains information about marketing campaigns across TV, radio, and social media, as well as how much revenue in sales was generated from these campaigns.
Based on this information, company leaders will make decisions about where to focus future marketing resources. Therefore, it is critical to provide stakeholders with a clear understanding 
of the relationship between types of marketing campaigns and the revenue generated as a result of this investment.

# Business Statement
Formulate a model that determins the impact of radio compaign on sales.

![image](https://github.com/user-attachments/assets/3bb71b3f-5735-4dab-b1d3-f8e716c4072d)
![image](https://github.com/user-attachments/assets/ace7ce5b-b5f3-4271-b741-8b1507d91629)
![image](https://github.com/user-attachments/assets/37e4e1d6-d321-4275-8682-50bc44439f06)

- There are 3 rows containing missing values, which is not that many, considering the total number of rows.
  It would be appropriate to drop these rows that contain missing values to proceed with preparing the data for modeling.

### Drop the rows that contain missing values.
This is an important step in data cleaning, as it makes the data more usable for the analysis and regression that you will conduct next.

![image](https://github.com/user-attachments/assets/2808b16c-9145-47fd-9b75-ce87e1009e5b)

### Check model assumptions.
I would like to explore the relationship between radio promotion budget and sales using linear regression. 
To do this, I would like to check if the model assumptions for linear regression can be made in this context. 
I would want to check the relationship in the between variables in the dataset before the model is built.

![image](https://github.com/user-attachments/assets/7178b206-090d-451c-badd-337f2c397c5d)

- In the scatter plot of `Sales` over `Radio`, the points appear to cluster around a line that indicates a positive association between the two variables.
  Since the points cluster around a line, it seems the assumption of linearity is met.

  ![image](https://github.com/user-attachments/assets/fa87c75a-138a-435e-b78c-5f99ccb8fb76)
  ![image](https://github.com/user-attachments/assets/7886e937-89f7-4346-86e9-14b424638d4e)

  ### Analyze the bottom table from the results summary.
From the summary of the model;
- The y-intercept is 41.5326. 
- The slope is 8.1733. 

Now I can express the relationship between sales and radio promotion budget in the form of y = slope * x + y-intercept
- sales = 8.1733 * radio promotion budget + 41.5326
- The model above indicates that if a company decides to buy 1 million dollars more for promoting their products/services on the radio, the company's sales would increase by 8.1733 million dollars on average.
  
 ### Checking the rest of the model assumptions.
After building the model, it's also important to check the rest of the model assuptions which will also help in confirming my findings.

### Plot the OLS data with the best fit regression line.
![image](https://github.com/user-attachments/assets/7fc77c5e-f29d-4d42-ad9c-38cd61f93772)

- The above regression plot illustrates an approximately linear relationship between the two variables along with the best fit line.
  This confirms the assumption of linearity. I would like to continue to check the other assumptions on the model.

  ![image](https://github.com/user-attachments/assets/26b262a2-122a-44e3-9687-4d0364e34c3b)

- Based on the preceding visualizations, the distribution of the residuals is approximately normal.
- In the Q-Q plot, the points closely follow a straight diagonal line trending upward. This confirms that the normality assumption.
- In the scatterplot, the data points have a cloud-like resemblance and do not follow an explicit pattern.
  So it appears that the independent observation assumption has not been violated. Given that the residuals appear to be randomly spaced, the homoscedasticity assumption is met.

  ## Conclusion
* The results of a linear regression model can be used to express the relationship between two variables. 
* In the simple linear regression model, the y-intercept is 41.5326 and the slope is 8.1733. This means,
  if a company buys 1 million dollars more for promoting their products/services on the radio, the company's sales is likely to increase by 8.1733 million dollars on average.
* The results are statistically significant with a p-value of 0.000, which is a infinitesmally small value which is smaller than common significance level of 0.05.
  This indicates that there is a very low probability of observing data as extreme or more extreme than this dataset when the null hypothesis is true. 

### Hypothesis Testing
* Null hypothesis : There is no relationship between radio promotion budget and sales i.e. the slope is zero.

* Alternative hypothesis : There is a relationship between radio promotion budget and sales i.e. the slope is not zero. 
   * Base on the model, I reject the null hypothesis, hence there is a relationship between radio promotion budget and sales.

* The slope of the line of best fit that resulted from the regression model is approximate and subject to uncertainty.
  The 95% confidence interval for the slope is from 7.791 to 8.555. This indicates that there is a 95% probability that the interval [7.791, 8.555] contains the true value for the slope.
  
* Based on the dataset at hand and the regression analysis conducted, there is a notable relationship between radio promotion budget and sales for companies in this data,
  with a p-value of 0.000 and standard error of 0.194. It would be worth continuing to promote products/services on the radio.
  Also, it is recommended to consider further examining the relationship between the two variables (radio promotion budget and sales) in different contexts.
  For example, it would help to gather more data to understand whether this relationship is different in certain industries or when promoting certain types of products/services. 




