# Real-Life Application Of Various Statistical Techniques on Adidas Retail Dataset

## Table of contents

- [Introduction](#introduction)
- [Dataset Overview and Preparation](#dataset-overview-and-preparation)
- [Descriptive Statistics](descriptive-statistics)
- [Objective](#objective)
- [Testing Parametric Test](#testing-parametric-test)
- [Application of Statistical Techniques](#application-of-statistical-techniques)
- [One Way Anova](#one-way-anova)
- [Multiple Regression](#multiple-regression)
- [Variance Inflation Factor](#variance-inflation-factor)
- [One Sample T.Test](#one-sample-t-test)
- [Pearson Correlation](#pearson-correlation)
- [Kruskal Wallis](#kruskal-wallis)
- [Mood’s Median Test](moods-median-test)
- [Chi Squared](#chi-squared)
- [Conclusion](#conclusion)


# Introduction
The statistical analysis involves understanding the application of various statistical techniques and their real-life applications. this assessment focused on selecting and applying the appropriate statistical methods to this dataset ‘RetailSet’. The primary objective is to gain a comprehensive understanding of the dataset’s characteristics and extract valuable insights for informed decision-making in addressing business challenges. The analysis includes extensive Exploratory Data Analysis (EDA) using histograms and box plots to uncover patterns, correlations, and meaningful insights within the data.
Additionally, the assessment employs comprehensive skills in hypothesis testing and statistical analysis to address and investigate complex business challenges. The statistical techniques used in the case study include parametric tests such as the t-test and ANOVA, as well as non-parametric tests like the Wilcoxon Rank-Sum Test and the Kruskal-Wallis Test. These techniques are applied to assess the impact of different variables on sales performance, evaluate the influence of sales methods on profit, and understand regional variations in sales performance. The findings from these analyses provide valuable insights for optimizing retail sales strategies, tailoring marketing and sales strategies to regional preferences, and optimizing resource allocation.

# Dataset Overview and Preparation
This dataset was originally obtained from Kaggle, the dataset is Adidas retail dataset, and it has been processing and clean to ensure thorough analysis. The data transformation is executed with precision using Python. The transformation ensures its reliability for statistical techniques. The dataset has 1800 observations and 11 variables covering attributes such as Year, Region, State, City, Product, Unit_Price, Units, Sales, Profit, Margin, and Sales_Method, it offers a rich source for uncovering meaningful insights. The reprocessing ensures accuracy, reliability, and relevance for a comprehensive Exploratory Data Analysis (EDA), With the aim of revealing patterns and extracting valuable insights using Statistical Technique. The link for the dataset can be found in the reference section.


## Loading and Preparing the Dataset for Analysis
The dataset “RetailSet_Data.csv” has been successfully imported. The dataset contains valuable information for analysis, and I’ll proceed with a comprehensive exploration to derive meaningful insights.

## Performing an In-Depth Exploratory Data Analysis (EDA)
To understand the recent changes in the retail store through the data, it involves conducting a thorough Exploratory Data Analysis (EDA) on the RETAILSET dataset. By leveraging histograms and box plots to check the distribution, The aim to swiftly gain a clear understanding of the data’s spread, central tendency, and potential outliers. This analysis will assist in identifying patterns, making well-informed decisions about data pre-processing, and extracting valuable insights for subsequent analyses.

![Screen Shot 2024-07-04 at 17 40 59](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/feaddfc3-5d07-4d9c-a9b9-cdcea9070f0b)

## Descriptive statistics
![Screen Shot 2024-07-04 at 17 43 43](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/e9540387-6cdb-4a40-9fca-f1278ce682e9)![Screen Shot 2024-07-04 at 17 45 25](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/87ed17cf-3b50-442a-ad8e-746dd68d9a61)


### Ensure Data Quality: Detecting Duplicates and Missing Values
![Screen Shot 2024-07-04 at 17 46 59](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/322e9163-dd3d-4fb7-98fd-0e5bb37e13f5)

Inference: The dataset has been thoroughly analyzed to identify any duplicate rows, and I’m pleased to say that no duplicates Ire detected. The absence of duplicate rows ensures the integrity of the dataset and reduces redundancy in our upcoming analyses. I have also conducted a thorough check for missing values to confirm that the dataset is complete and dependable. This preliminary assessment provides a solid basis for future analyses and strengthens the cleanliness and reliability of our dataset. As I continue to conduct exploratory data analysis as well as statistical technique tests, the absence of duplicate rows and missing values instill confidence in the reliability of my findings.

# Objective
Optimizing Retail Strategies by Unveiling Insights and Patterns through Comprehensive Exploratory Data Analysis (EDA) And Statistical Technique.
The retail store aims to extract valuable insights from the RetailSet dataset to enhance sales performance, focus on the target variables “Sales”, “Unit_Price”, “Profit”. Our objectives include identifying the most effective sales methods, evaluating the impact of promotional strategies based on a previous sale average (50), and assessing the influence of unit price, region, and unit quantity on sales and profit.
Problem Statement:
1. I’m investigating the impact of sales methods, categorized as ‘Online’, ‘Outlet’, ‘In-store,’ on sales figures in a retail dataset. Understanding the impact of different sales methods on sales figures is crucial for optimizing our sale strategies and resource allocation.
2. The retail store seeks to investigate the factors influencing profit outcomes, specifically examining whether the unit price, product, and region significantly contribute to variations in profits.
3. The retail store is curious to know if the recent sales figures show a meaningful shift from our usual average of 100,000, potentially influenced by early bulk supply. In simpler terms, I want to see if there’s a real impact on sales. Is the current sales average significantly different from our usual benchmark of 100,000.
4. To optimize revenue effectively, I aim to explore the relationship between sales and profit strategies. The key question is whether there is a clear connection between sales and the resulting profit.
5. The retail store aims to understand if there are significant differences in sales performance among different regions. This insight is crucial for tailoring marketing and sales strategies to regional preferences and optimizing resource allocation.
6. The retail store aims to explore whether there are significant differences in profit across different cities, specifically investigating if the median profits vary among these locations. This analysis is crucial for tailoring localized strategies and resource allocation.
7. The retail store is interested in assessing whether there is a significant association between the categorical variables “Region” and “Sales_Method” in the retailset dataset.
   
![Screen Shot 2024-07-04 at 17 49 21](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/79740d57-845f-4845-8052-76de7f1c5127)
![Screen Shot 2024-07-04 at 17 49 48](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/ee8d17ec-3052-407f-834d-f0a4773fc7b7)

Histrogram Observation: The visual analysis of the histogram above reveals distinct distribution patterns within the dataset. Both unit price, Sales shows a symmetric, bell-shaped distribution that indicate of normal distribution. while the profit is right-skewed, the peak of the distribution is on the right side, which implying a slight bias towards higher profit values. These insights enhance our understanding of the dataset’s underlying characteristics, providing valuable context for further analysis when deciding the statistical technique to use to solve the casestudy.
Boxplot Observation: Boxplots above shows that data is not normally distributed around the mean and is skewed towards one side. Profit boxplot above has a longer whisker and outliers on one side that shows a skewed distribution, while Unit_Price and Sales shows a roughly normal distribution as both whiskers are of similar length and the median is in the centre of the box, still appears to have unusual values as there are outliers. However, profit plot is right-skewed (postively skewed) that show that profit does not meet one the parametric assumption.

# Testing Parametric Test
Verifying for parametric Assumptions for the Target Variable. This is a process of assessing whether the target variables (Sales, Unit_Price, Profit) satisfies the assumptions required for parametric tests. parametric tests assume specific characteristics about the underlying distribution of the data. These assumptions include normality, homogeneity of variances, and independence, among others. For this project, I’m checking whether the target variable meets only normality assumptions, which is crucial before applying parametric tests.

### Assessing Normality Assumption: QQ Plot and Shapiro-Wilk Test

I will conduct a normality assessment using the Shapiro-Wilk test and also use QQ plot, a suitable approach given the sample size exceeding 30. 

![Screen Shot 2024-07-04 at 17 50 57](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/8be966db-e493-4e12-b1dc-3f5096df21ae)


Inference: Unit_price and Sales appears to follow a normal distribution, The p-values of Sale (0.82940) and p- value of Unit_Price (0.3848) are both higher than the significance level (0.05) based on the Shapiro-Wilk test, there is no strong evidence to conclude that the Sales and Unit_Price variables do not follow a normal distribution. A parametric test can now be conducted on the Sales and Unit_Price variables to gain insights into these two variables in the dataset. Currently, I’m specifically testing for normality out of the four assumptions required for parametric tests. Confirming normality is crucial, as it implies that the remaining assumptions are satisfied based on the normal distribution of the available data.

### Q-Q plot
Other methods to test for normality include Q-Q plots. A Q-Q plot, short for quantile-quantile plot, compares the quantiles of the observed data against the quantiles of a theoretical normal distribution. It provides a visual assessment of how closely the data follows a normal distribution. The Q-Q plot for the target variables— Unit_Price, Sales, and Profit—will be plotted below to assess the normality assumption also. 

![Screen Shot 2024-07-04 at 17 51 36](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/64bcb8db-ac48-483e-a48b-5b2bc39967a5)
![Screen Shot 2024-07-04 at 17 52 01](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/db660b72-d055-4f37-8cb7-2b66b9aac95f)


Inference: The data points for (Sales and Unit_Price) roughtly fall along a straight diagonal line in a Q-Q plot, the show that dataset likely follows a normal distribution.

# Application of Statistical Techniques
I’m embarking on the application of various statistical techniques, as the selected variables in the dataset have successfully met the assumptions required for various statistical analyses. This ensures the reliability and validity of the results obtained from each applied statistical method in addressing specific problem statements.

### One Way Anova
Problem Statement 1:
I’m investigating the impact of sales methods, categorized as ‘Online’. ‘In-store, Outlet’ on the sales figures. Hypotheses:
• Null Hypothesis (H0): No significant difference in mean sales figures across sales methods; any observed variation is random.
• Alternative Hypothesis (H1): There’s a significant difference in mean sales figures across sales methods; variation is not solely random, indicating a meaningful relationship.

Methodology:
The statistical technique that will be employed is one-way ANOVA to compare the means of sales figures across different sales method groups. Anova (Analysis of Variance) test allows the comparison of the means of three or more independent groups, “Sales_Method” has more than two levels, so I can’t use Two sample T-Test. That is why anova is the suitable one. Understanding how different sales methods influence sales performance is crucial for optimizing business strategies and resource allocation.

### Parametric Test: One-Way Anova
![Screen Shot 2024-07-04 at 17 52 47](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/5495a375-1bde-4238-8b83-b7822ef25d4e)

Inference: The p-value of the Sales Method is 0.201, is not less 0.05, therefore the null hypothesis (HO) will not be rejected. This means there is no significant difference in mean sales figures between the “Online” and “In- store” sales methods. The observed variation in sales figures appears to be random, and there is insufficient support to claim a meaningful relationship between sales method and sales performance in this dataset. This result indicates that, based on the current analysis, business strategies and resource allocation may not need to be adjusted based on the distinction between “Online” and “In-store” sales methods.

### Multiple Regression
Problem Statement 2:
The retail store seeks to investigate the factors influencing profit outcomes, specifically examining whether the unit price, product, and region significantly contribute to variations in profits.

Hypotheses:
• Null Hypothesis (H0): The unit price, product, and region do not have a significant impact on profits.
• Alternative Hypothesis (H1): At least one of the variables (unit price, product, region) has a significant
impact on profits.

Methodology:
To achieve this, a regression model will be used to assess the impact of these factors on profits. The model will help in understanding how unit price, product, and region all influence profit, which is crucial for optimizing business strategies and resource allocation.
When using a categorical variable in multiple regression, it needs to be converted into dummy variables to facilitate its inclusion in the model. Categorical variables, like “Product” or “Region,” have discrete categories without inherent numerical order. Regression models require numerical input, and dummy variables helps convert these categories into a format suitable for regression analysis.
Each level of a categorical variable is represented by a binary indicator (dummy variable), and for a categorical variable with k levels, k−1 dummy variables are created. Including all levels of a categorical variable without creating dummy variables could lead to multicollinearity issues. Therefore, dummy variables help avoid perfect correlation between the predictors, ensuring numerical stability in the regression model
![Screen Shot 2024-07-04 at 17 54 19](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/470bdcaf-5cb9-4311-b94a-ea60d04b668e)


Inference: The regression model aims to predict profit based on unit price, product type, and region. Here’s the Inference of the key components: The p-values provide insights into the significance of the predictors in the multiple regression model. The intercept has a highly significant p-value, indicating that the estimated profit is significantly different from zero when all other predictors are zero. HoIver, the unit price does not have a significant effect on profit, as its p-value is (0.412).
Among the product categories, “Men’s Street FootIar” and “Women’s Apparel” have significant positive effects on profit, as their p-value is obviously less than 0.05, while “Men’s Athletic” and “Women’s Athletic” do not. In terms of regions, “Northeast,” “South,” “Southeast,” and “Ist” all have significant effects on profit. The overall model is significant, suggesting that at least one predictor variable significantly contributes to the model.The Multiple R-squared and Adjusted R-squared values suggest that the model explains around 14.86% of the variance in profit. The residuals have a mean of approximately zero, indicating a good fit. To confirm the fitting of the regression model without assumption, I’m going to test the fitting using VIF (Variance Inflation Factor)
 
### Variance Inflation Factor
To calculate the fitting the regression model. The VIF will help me to assesses the level of multicollinearity among the predictor variables in the regression model. Multicollinearity is a condition where two or more predictor variables in a regression model are highly correlated, which makes it challenging to determine the individual contribution of each variable, if high multicollinearity is detected, I may need to address it. This could involve removing one of the correlated variables, combining variables, or using other advanced techniques.

![Screen Shot 2024-07-04 at 17 54 52](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/601bb08d-d20b-49e5-8404-756f137ce337)


Inference: For each predictor in my model unit_price, Product, and Region, The VIF values above indicate low levels of multicollinearity. Each predictors have their independence, that indicate a reliable Inference in the regression model. for Unit Price is approximately 1.0059. with a GVIF close to 1, there is minimal evidence of multicollinearity associated with Unit Price, suggesting that it does not significantly contribute to increased variance in the regression coefficients.
The VIF for Product is around 1.0098. While there is a slight increase in variance due to potential multicollinearity, it remains relatively low. The seven degrees of freedom indicate the number of levels in the categorical variable “Product. The VIF for Region is approximately 1.0090. Similar to Product, there is a minor increase in variance, but it remains at an acceptable level. The four degrees of freedom correspond to the levels in the categorical variable “Region”.

### One-Sample T-Test 
Problem Statement 3
 The retail store is curious to know if the recent sales figures show a meaningful shift from the usual average of 100,000, potentially influenced by early bulk supply. In simpler terms, I want to see if there’s a real impact on sales. To do this, I will be running a one-sample t-test, checking if the current sales average is significantly different from the previous average sale of 100,000.
 
Hypotheses:
• Null Hypothesis (H0): The mean sales figure remains unchanged and equals $100,000.
• Alternative Hypothesis (H1): There is a significant difference in the mean sales figures, suggesting an impact from early bulk supply.

![Screen Shot 2024-07-04 at 17 55 56](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/9097d76c-d5c4-4e4a-a4f2-f36fb1ad8d1e)

Inference: The p-value (2.2e-16) is less than our signifance level =0.05, The null hypothesis is rejected, this shows sufficient evidence that the mean of the recent sales figures significantly differs from our previous sales average of $100,000. The P-Value shows that tangible impact of early bulk supply on the current sales figure. To understand if there is an increase or decrease. I will conduct a One-Tailed Test, for greater and less.

### Utilizing the One-Sample T-Test in a One-Tailed Analysis
To perform a one-tailed test with the one-sample t-test, Testing using a one-tailed test to know whether the recent sales figures are significantly greater or less than the usual average of $100,000.

![Screen Shot 2024-07-04 at 17 57 13](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/9f09b50e-392d-425b-b8a3-961eef74a2f3)
![Screen Shot 2024-07-04 at 17 57 34](https://github.com/AdedotunTemi/Data-Analysis-Application-of-Statistical-Technique--R/assets/168010102/727aea12-40ed-478d-b85a-e3103161c995)



Inference: In the conducted one-tailed test above, the alternative hypothesis state that the true mean of sales is greater than $100,000. The extremely low p-value (< 2.2e-16) indicate strong evidence to conclude that our current sales average figure is significantly higher than the previous average sales of 100,000.

### Pearson Correlation
Problem Statement 4:
To optimize revenue effectively, I aim to explore the relationship between sales and profit strategies. The key question is whether there is a clear connection between sales and the resulting profit.

#### Hypotheses:
• Hypothesis: Null Hypothesis (H0): There is no significant correlation between sales and profit.
• Alternative Hypothesis (H1): There is a significant correlation between sales and profit.

Methodology: I will employ the Pearson correlation, which enables me to measure the strength and direction of a linear relationship between two continuous variables: Sales and Profit. This statistical technique will uncover a meaningful and statistically significant connection between sales and the resulting profit, it will also offer valuable insights into the connection between these two critical variables, with values ranging from -1 (indicating a perfect negative correlation) to 1 (indicating a perfect positive correlation), and 0 indicating no correlation. This will aid in developing revenue optimization strategies

![Screen Shot 2024-06-18 at 17 52 51](https://github.com/AdedotunTemi/Application-of-Statistical-Technique-on-Data-Analysis-R/assets/168010102/81c2125a-304c-4d2e-b0bf-b08ef077f094)
![Screen Shot 2024-06-18 at 17 54 32](https://github.com/AdedotunTemi/Application-of-Statistical-Technique-on-Data-Analysis-R/assets/168010102/6119b749-abfa-4c08-a67d-721bc731f5fc)
![Screen Shot 2024-06-18 at 17 54 53](https://github.com/AdedotunTemi/Application-of-Statistical-Technique-on-Data-Analysis-R/assets/168010102/aab53268-28d3-41be-9c04-3cd99d162ed1)

Inference:The p-value of 0.5617 shows that there is no significant evidence to reject the null hypothesis of no correlation between “Sales” and “Profit.” which indicate that the observed correlation between sales and profit could likely be due to random chance. Therefore, based on this p-value, I fail to reject the null hypothesis, there is no strong linear relationship between sales and profit in the dataset. coefficient may indicate a numerical relationship between the variables, the p-value helps assess the statistical significance of that relationship. The correlation coefficient between “Sales” and “Profit” is approximately [0.01368672].
This value is close to zero, suggesting a very weak positive correlation between sales and profit. A correlation coefficient close to 0 indicates a weak or no linear correlation. The correlation between sales and profit is very weak, suggesting that the two variables do not have a strong linear relationship. It implies that changes in sales are not strongly associated with changes in profit in a linear fashion based on the given dataset. Other factors or non-linear relationships may be influencing the relationship between sales and profit.

### Kruskal Wallis 
Problem Statement 5:
The retail store aims to understand if there are significant differences in profit outcomes among different regions. This essential for providing valuable insights for optimizing business strategies across diverse geographic areas.

Hypotheses:
• Null Hypothesis (H0): There is no significant difference in profit among different regions.
• Alternative Hypothesis (H1): There is a significant difference in profit among different regions.

Methodology: I’m examining profit across various regions, and the Kruskal-Wallis test will allow me to assess whether these regional differences are statistically significant without assuming a normal distribution in the data. Kruskal-Wallis test determine whether or not there is a statistically significant difference between the medians of three or more independent groups. which is suitable when dealing with a variable like profit that does not follow a normal distribution. To assess regional profit variations without assuming a normal distribution, using a non- parametric approach.

### Non-Parametric Tests - Kruskal-Wallis Test:
![Screen Shot 2024-06-18 at 17 56 48](https://github.com/AdedotunTemi/Application-of-Statistical-Technique-on-Data-Analysis-R/assets/168010102/bd27e2ab-3375-4c5f-a9f0-9d7e260495e0)

Inference: The Kruskal-Wallis test results shows that there is a significant difference in profit among different regions. (p-value < 2.2e-16). This indicates that there is strong evidence to reject the null hypothesis, suggesting that the median Profit across the various regions are significantly different. Therefore, I do have sufficient evidence to conclude that at least one of the groups has a different median profit from the others.

## Mood’s Median Test
 The retail store aims to explore whether there are significant differences in profit across different cities, specifically investigating if the median profits vary among these locations such as birmingham, portland, louisvil and others. This analysis is crucial for tailoring localized strategies and resource allocation.
 
Hypotheses:
• Null Hypothesis (H0): There is no significant difference in the median profit among different cities.
• Alternative Hypothesis (H1): There is a significant difference in the median profit among different cities.
Methodology: To investigate this, I will employ Mood’s Median Test, a non-parametric test suitable for comparing medians across multiple independent groups. This test does not assume a specific distribution of the data. It is a distribution-free test, and is well-suited for ordinal or categorical data. I’m going to examine the “City” frequency table to understand the distribution of the categorical variable “City”. To ensure that I have enough observations in each group.

![Screen Shot 2024-06-18 at 17 57 47](https://github.com/AdedotunTemi/Application-of-Statistical-Technique-on-Data-Analysis-R/assets/168010102/8bb60f2b-c352-4d6d-83db-89b918445a3b)
![Screen Shot 2024-06-18 at 17 58 05](https://github.com/AdedotunTemi/Application-of-Statistical-Technique-on-Data-Analysis-R/assets/168010102/19fa9ff2-e45a-48c2-a6e6-5123f02172f0)

Inference: The Asymptotic K-Sample Brown-Mood Median Test was conducted to assess whether there are significant differences in profit across various cities. The low p-value (< 2.2e-16) indicates strong evidence against the null hypothesis (H0), that there is no significant difference in the median profit across different cities. Therefore, I reject the null hypothesis in favor of the alternative hypothesis (H1). This suggests that there is a significant difference in the median profit among the cities represented in the dataset. The results of the Mood’s Median Test imply that the profitability of the retail store varies significantly across different cities.

## Chi Squared 
Problem Statement 7:
The retail store is interested in assessing whether there is a significant association betweenthe categorical variables “Region” and “Sales_Method” in the retailset dataset. Specifically, the goal is to determine if the distribution of sales methods varies across different regions.

Hypotheses:
• Null Hypothesis (H0): There is no significant association between “Region” and “Sales_Method.”
• Alternative Hypothesis (H1): There is a significant association between “Region” and “Sales_Method.”
Methodology: To achieve this, I’ll be using Chi-squared test, Chi-squared tests are especially useful when dealing with categorical data, where observations are classified into distinct categories. it’s helps in assesses whether the observed distribution of categories in one variable is independent of the categories in the other variable.

### Chi-Square Tests:
![Screen Shot 2024-06-18 at 17 59 00](https://github.com/AdedotunTemi/Application-of-Statistical-Technique-on-Data-Analysis-R/assets/168010102/931b1d70-c419-4cd0-8e6d-9d08f7c262a7)

Inference: The contingency table summarizes the distribution of sales methods (“In-store,” “Online”, “In-store”) across different regions (Midwest, Northeast, South, Southeast, and west). The counts in the table represent the number of occurrences for each combination of region and sales method. The Pearson’s Chi-squared test was conducted to determine if there is an association between the region and the sales method. The test resulted in a chi-squared statistic of (463.17) with 8 degrees of freedom and a p-value less than 2.2e-16, Which indicate a highly significant association between the region and the sales method. Therefore, I reject the null hypothesis of independence and conclude that the region is associated with the sales method. The result suggests that the choice of sales method may be influenced by the region, and vice versa, in the retail dataset.

### Conclusion
Statistical techniques applied on the ‘Retailset’ dataset has really provides valuable insights into retail dynamics. The analysis covers exploratory data analysis, parametric and non-parametric tests, regression modeling, and chi-square tests. The findings generate from this analysis will contribute to the informed decision- making processes for optimizing retail sales strategies, It enable me to have understand of the impact of different variables. The results indicate so many insights information, showing an evident that there is significant association between the region and the sales method, also suggested that the choice of sales method may be influenced by the region, and vice-versa, in the retail dataset.
I’m able to derive many answers to the business problem statement, Additionally, the regression model has also help us to understand and assess the impact of the unit price, product, and region on profits, providing further insights into the factors influencing profit outcomes in the retail store. The effective application of statistical techniques is essential for extracting meaningful insights, validating hypotheses, and making informed decisions in a data-driven environment. Understanding the nature of the data, select the appropriate statistical tools, and evaluate your assumptions critically to ensure the accuracy and validity of your analytical results. As we move into the era of large data, statistical literacy has become a key competency for researchers and analysts, also as decision-makers, to make the most of data and achieve meaningful results.

