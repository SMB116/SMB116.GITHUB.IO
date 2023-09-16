***What's Age Gotta Do with It? More Than We Know..***

The old saying, "age is nothing but a number," can hold a different meaning in the workplace. As an intern in IBM's Data Analyst team, I found myself questioning the significance of age within our professional realm. Recent waves of employees departing from our organization have brought age into the spotlight, making me wonder: Could it be more than just a number when it comes to attrition? Using the statistical power of R, I aim to determine whether age has a significant statistical impact on attrition within our organization.

**The Dataset**

The dataset at hand, crafted by IBM's data experts, provides valuable insights. It consists of 1470 rows, each representing an employee, and boasts 35 columns filled with information. 

At the heart of our exploration is the "Attrition" column. It tells us whether an employee left or stayed. While we're not entirely sure if "Attrition" includes voluntary departures, layoffs, or both, for our analysis, we'll focus on voluntary exits.

**Our Mission**

With this data, my mission is clear: to uncover the connection between age and attrition within our organization. While we've heard that younger employees tend to leave more, we want to dig deeper. We're looking for the details that can shape our HR strategy, ensuring we keep our team engaged and strong.

**Key Insights:**

1. Age and Experience: **Employee age strongly correlates (0.68) with total working years**, indicating longer service as employees age.
2. Income Connection: Age correlates positively with monthly income, suggesting higher incomes for older employees.
3. Attrition Impact:**Age significantly impacts attrition**; younger employees tend to leave, while older ones stay. Both t-test and Chi-Square tests confirm this trend.
4. Age Profile: **Our workforce is predominantly young, with an average age of 37**and a positive skew toward younger ages.
5. Predictive Power: **Age alone explains 25% of income variance**. Combining age and total working years raises the R-squared to 0.5988, highlighting their role in income prediction.
6. Attrition Patterns: Attrition varies among age groups. Notably, only the 26-35 and 56-60 groups retain a significant portion of employees. Surprisingly, the **36-45 to 45-55 groups, with seasoned employees, show unexpected attrition trends**.

**Age Distribution**

Our initial exploration of employee age distribution reveals a fascinating pattern. 

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/e621eb45-29f4-41e3-b41e-d76260f47945)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/8e5a602e-f891-4332-876c-106f05beecb5)

The histogram of age data shows a positive skew, indicating that a significant portion of our workforce consists of younger individuals. The majority of our employees, with a peak frequency occurring at the lower ages, suggest that our organization has a predominantly younger workforce, with an average age of approxiately 37.

**Correlations**
Digging deeper, we explored correlations between various factors. 

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/f541e4dd-e312-440a-aee9-e0983eaf7198)

Notably, we discovered a strong correlation between age and total working years, suggesting that as employees grow older, their total years of service tend to increase. Furthermore, age and total monthly income also exhibit a positive correlation, albeit with some exceptions. This implies that, in general, older employees tend to have higher monthly incomes.

**Age and Attrition**

The crux of our investigation centers around the relationship between age and attrition. Initial observations from box plots hint at a difference in attrition rates between age groups.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/41b8e563-7684-465f-9d01-552a6abc8ae6)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/ca5df7b9-2438-4aa6-b295-da734a7c1cd3)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/21a3a0b0-f0cb-4e1e-9253-050fabe71680)

To rigorously test this, we conducted a t-test, and the results were striking. The extremely low p-value (e.g., 1.38e-08) provided robust statistical evidence against the null hypothesis. We confidently reject the null hypothesis and accept the alternative hypothesis that age and attrition are indeed interconnected.


**Chi-Square Test**

To strengthen the credibility of our findings, we took a closer look by categorizing employees into distinct age groups and subjecting them to a rigorous Chi-Square test. 

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/0de2a494-1b23-4c6e-a78b-a892b7469c33)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/d38daeab-ce1e-46f6-ac63-dd787b938c05)

The results were nothing short of astonishing, revealing an incredibly low p-value, approximately 4.341e-11. This outcome underscores a substantial and non-random connection between age groups and attrition within our organization. In practical terms, it indicates that attrition rates exhibit significant variations across different age groups in our dataset, firmly establishing age as a pivotal factor when deciphering the intricacies of attrition patterns.

**Visualization Context:**
To provide additional clarity, let's delve into the visualization:

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/184b87ca-cde3-49d0-b70f-b9fe011859de)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/70ffe5d7-53ff-4231-8500-11b5a48b3411)

- The **blue bars** represent employees who left the company (attrition = "Yes").
- The **red bars** represent employees who stayed with the company (attrition = "No").

These color cues offer a straightforward way to understand the attrition status within each age group. But what does it mean when you see approximately 20% for both the blue and red bars within each age group? It signifies a vital insight:

- About 20% of the employees in that age group chose to explore new horizons (indicated by the blue bars).
- Approximately 80% of the employees in that age group decided to continue their journey with our company (indicated by the red bars).

What's truly interesting is that only two age groups, the 26-35 and 56-60 brackets, appear in red. One could speculate on possible reasons for this intriguing pattern. 

It's conceivable that the 26-35 age group may find themselves in a relatively comfortable position in life, less inclined to explore new opportunities, and perhaps more content in their roles. Conversely, the 56-60 age group, nearing retirement age, may be firmly established in their careers, making the prospect of leaving less appealing. 

However, it's the data concerning the 36-45 to 45-55 age groups that raises eyebrows and concerns. These cohorts represent some of our more seasoned employees, individuals with valuable experience and expertise. The fact that they are opting to leave warrants a closer look and raises important questions about what might be driving this unexpected trend.

**Income-Age Relationship: A Linear Regression Exploration**

As we delve deeper into the relationship between age and various aspects of employment, we turn our attention to predictive modeling. Specifically, we've created a linear regression model that predicts MonthlyIncome based on age. The power of R makes this task remarkably straightforward. We utilize the 'lm' function, short for linear model, to build our predictive model. 

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/55e6606b-51a5-48af-b2db-4a6e45b375e9)

To gain insights into the model's performance, we invoke the 'summary' function with 'summary(model1)'. The results provide us with valuable information, including the R2 value, which quantifies the model's explanatory power. 

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/e957a146-ea65-4302-b86a-77aca6d888d7)

In our case, the R2 value is 0.2479, indicating that age can explain approximately 25% of the variance in MonthlyIncome. Moreover, the model's p-value is nearly 0, signifying its statistical significance with 95% confidence. This model illustrates how age alone can serve as a predictor of MonthlyIncome, but it's just the beginning. In future analyses, we can explore more complex models with multiple variables, paving the way for a deeper understanding of the factors influencing our workforce.

In our quest to understand the dynamics of income within our workforce, we've ventured further into the realm of predictive modeling. Building upon our initial linear regression model, which solely considered 'Age' as a predictor of 'MonthlyIncome,' we've taken a more comprehensive approach. In this new model, named 'model2,' we incorporated 'TotalWorkingYears' alongside 'Age' as predictors.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/1437d366-18f6-4a5c-b1ba-f556e8c97877)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/2831cbf3-c713-4b1c-95d1-08b6020d791e)

The results are striking: the model's R-squared value has surged to 0.5988, signifying a substantial improvement in its ability to make clear the variations in 'MonthlyIncome.' Equally noteworthy is the remarkably low p-value of 2.2e-16, reaffirming the model's resounding statistical significance. This expansion of our analysis underscores the intricate interplay between age, total working years, and monthly income within our organization, shedding light on factors that contribute significantly to earnings

**Key findings:** 

1. Age and Total Working Years Correlation: A robust **positive correlation (0.68) exists between employee age and total working years, indicating that as employees age, their years of service tend to increase**.
2. Age and Monthly Income: Age demonstrates a positive correlation with total monthly income, implying that older employees generally have higher incomes.
3. Age and Attrition: **Age significantly influences attrition**, with younger employees more prone to leaving, while older employees tend to stay. This conclusion is supported by both t-test and Chi-Square test results with exceptionally low p-values.
4. Age Distribution: Our employee age distribution exhibits a positive skew, centered around lower ages, indicating a predominantly **youthful workforce with an average age of around 37**.
5. Predictive Modeling: **Age alone can explain approximately 25% of the variance in MonthlyIncome**, underscoring its relevance as an income predictor. When combined with total working years, the R-squared value rises to 0.5988, emphasizing the intricate interplay between age, total working years, and income.
6. Attrition Patterns: Attrition rates diverge across age groups. Only the 26-35 and 56-60 age cohorts display a substantial proportion of retained employees. Surprisingly, **the 36-45 to 45-55 age groups, comprising more experienced employees, exhibit unexpected attrition patterns warranting further investigation**. 

**Conclusion**

These findings have profound implications for our HR strategy. It's clear that age plays a pivotal role in attrition within our organization. While younger employees may be more prone to attrition, this insight allows us to take proactive measures to mitigate it. By crafting targeted HR policies and initiatives, we can foster a more engaged and loyal workforce across all age groups, ultimately enhancing our organizational stability and success.

In conclusion, our analysis of the relationship between age and attrition within our organization has yielded several key findings. We have established that age plays a significant role in attrition, with younger employees exhibiting higher turnover rates. Additionally, age correlates with other employment-related factors, such as total working years and monthly income. Our organization's age distribution, characterized by a predominantly younger workforce, further underscores the importance of age in our HR strategy. Predictive modeling has illuminated age as a predictor of monthly income, and the inclusion of total working years enhances this predictive power. Notably, intriguing attrition patterns emerged, with only the 26-35 and 56-60 age groups showing significant proportions of employees who stayed. This calls for a closer examination of the unexpected attrition trends among the 36-45 to 45-55 age groups. To address these findings, we recommend the implementation of age-diverse retention strategies, continuous monitoring, tailored development programs, open communication channels, support for employees nearing retirement, investment in data analytics, and a holistic focus on employee well-being. These recommendations aim to harness the insights gained from our analysis, fostering a stronger, more resilient workforce and securing a brighter future for our organization.
