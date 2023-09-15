***What's Age Gotta Do with It? More Than We Know..***

The old saying, "age is nothing but a number," can hold a different meaning in the workplace. As an intern in IBM's Data Analyst team, I found myself questioning the significance of age within our professional realm. Recent waves of employees departing from our organization have brought age into the spotlight, making me wonder: Could it be more than just a number when it comes to attrition? Using the statistical power of R, I aim to determine whether age has a significant statistical impact on attrition within our organization.

**The Dataset**

The dataset at hand, crafted by IBM's data experts, provides valuable insights. It consists of 1470 rows, each representing an employee, and boasts 35 columns filled with information. 

**The "Attrition" Column** 

At the heart of our exploration is the "Attrition" column. It tells us whether an employee left or stayed. While we're not entirely sure if "Attrition" includes voluntary departures, layoffs, or both, for our analysis, we'll focus on voluntary exits.

**Our Mission**

With this data, my mission is clear: to uncover the connection between age and attrition within our organization. While we've heard that younger employees tend to leave more, we want to dig deeper. We're looking for the details that can shape our HR strategy, ensuring we keep our team engaged and strong.

**Age Distribution**

Our initial exploration of employee age distribution reveals a fascinating pattern. 

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/42f0a322-c9c2-4ecd-a9e7-40eb435e1f64)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/8e5a602e-f891-4332-876c-106f05beecb5)

The histogram of age data shows a positive skew, indicating that a significant portion of our workforce consists of younger individuals. The majority of our employees, with a peak frequency occurring at the lower ages, suggest that our organization has a predominantly younger workforce, with an average age of approxiately 37.

**Correlations**
Digging deeper, we explored correlations between various factors. 

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/51b393ee-9642-47d0-adcd-c93028ce3988)

Notably, we discovered a strong correlation between age and total working years, suggesting that as employees grow older, their total years of service tend to increase. Furthermore, age and total monthly income also exhibit a positive correlation, albeit with some exceptions. This implies that, in general, older employees tend to have higher monthly incomes.

**Age and Attrition:**
The crux of our investigation centers around the relationship between age and attrition. Initial observations from box plots hint at a difference in attrition rates between age groups. To rigorously test this, we conducted a t-test, and the results were striking. The extremely low p-value (e.g., 1.38e-08) provided robust statistical evidence against the null hypothesis. We confidently reject the null hypothesis and accept the alternative hypothesis that age and attrition are indeed interconnected.


**Chi-Square Test:**
To further validate our findings, we conducted a Chi-Square test, which yielded an astonishingly low p-value of approximately 4.341e-11. This result underscores a significant and non-random association between age groups and attrition in our organization. In practical terms, it suggests that attrition rates vary significantly across different age groups within our dataset, making age a key factor in understanding attrition patterns.

**Visualization Context:**
To provide additional clarity, let's delve into the visualization:

- The **blue bars** represent employees who left the company (attrition = "Yes").
- The **red bars** represent employees who stayed with the company (attrition = "No").
When you see approximately 20% for both the blue and red bars within each age group, it means:
- About 20% of the employees in that age group left the company (indicated by the blue bars).
- About 80% of the employees in that age group stayed with the company (indicated by the red bars).
This context helps to clarify that the percentages represent attrition rates within each age group, highlighting the proportion of employees who stayed and those who left. It reinforces the significance of age as a factor in attrition within our organization.

**Implications and Future Steps:**
These findings have profound implications for our HR strategy. It's clear that age plays a pivotal role in attrition within our organization. While younger employees may be more prone to attrition, this insight allows us to take proactive measures to mitigate it. By crafting targeted HR policies and initiatives, we can foster a more engaged and loyal workforce across all age groups, ultimately enhancing our organizational stability and success.
**Conclusion:**
In conclusion, our analysis provides compelling evidence that age is indeed a significant factor in attrition within our organization. While younger employees may be more likely to leave, this insight empowers us to take strategic action. By embracing age-diverse retention strategies, we can build a stronger, more resilient workforce, securing a brighter future for our organization.
