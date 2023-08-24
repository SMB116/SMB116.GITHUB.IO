# Metals in Focus: Analyzing Iron Concentration Patterns in Mining 

## Shaping Our World: The Iron Story You Never Knew

Ever thought about what skyscrapers, bridges, cars, and even your home appliances have in common? It's iron! This metal is like the superhero behind the scenes, making all these things possible. But how does plain old iron become the magic ingredient that builds our world?

That's where I come in. I'm a data analyst at Metals R' Us, a mining company with a mission to extract and refine iron through a process that's as intricate as it is crucial. 

In our mining process, we start with clumps of dirt and rock containing iron hidden within. Through advanced techniques in our flotation plant, we unlock the iron's potential, ensuring the high-quality material that forms the backbone of structures and objects shaping our everyday lives.

## About the Dataset

The dataset contains **737,453 rows** and **24 columns**. If you want to access the data, you can find it on [Kaggle](https://www.kaggle.com/datasets/edumagalhaes/quality-prediction-in-a-mining-process). This dataset is sourced from real-world manufacturing plants, especially mining plants, making it a valuable resource for understanding real-world processes.

The main feature of primary interest in this dataset is `% Iron Concentrate`. This represents the purity and quality of the final iron product produced by the mineral processing plant. Metallurgists demand specific concentration grades from this product for smelting, making this value crucial in evaluating the effectiveness of the mineral processing operations.

To thoroughly investigate the quality of the concentrate products (`% Iron Concentrate`), several features will provide valuable support:

- `Iron Feed`: The initial iron content in the ore being processed.
- `Silica Feed`: The initial silica content in the ore.
- `Starch Flow`: The use of starch as a depressant for iron.
- `Amina Flow`: The use of amina to collect silica.
- `Ore Pulp Flow`: The flow of ore pulp into the flotation process.
- `Ore Pulp pH`: The pH level affecting chemical reactions.
- `Ore Pulp Density`: The solid density of the flotation feed.
- `Flotation Column Air Flow`: The amount of air affecting bubble formation.
- `Flotation Column Level`: The thickness of the flotation foam.

These features collectively offer valuable context and insights into how the processing plant's operational parameters influence the quality of the iron concentrate product.

# Key Takeaways:

1. **Correlation Analysis:** The correlation matrix highlights that there are no strong linear correlations among the variables "% Iron Concentrate," "% Silica Concentrate," "Ore Pulp pH," and "Flotation Column 05 Level." While the correlation coefficients suggest moderate relationships, this analysis doesn't account for potential non-linear connections or other influential factors in the dataset.

2. **Concentration Patterns:** A dip in both iron and silica concentrations during certain hours indicates potential issues in the flotation plant's separation process. Further investigation is needed to pinpoint the root causes, which could range from operational decisions to equipment performance.

3. **Iron-Silica Correlation:** The negative correlation coefficient of -0.8005 between iron and silica concentrations supports the expected inverse relationship. Higher iron content typically corresponds to lower silica content in the ore concentrate, aligning with mineral processing practices.

4. **Monthly Comparison (June and July):** Analyzing iron concentration averages for June and July highlights a consistent pattern of lower iron concentrations on Tuesdays. The average iron concentration on Tuesdays was 64.45 for June and 64.35 for July. This fluctuation indicates potential operational variations on Tuesdays in both months, with June showing greater overall variability.

5. **Monthly Variation:** Assessing iron concentration levels across different months reveals no consistent patterns. Fluctuations occur without a discernible trend, suggesting the influence of various dynamic variables. The absence of distinct trends emphasizes the complexity of iron concentration determinants.

# Let's Begin with Descriptive Analytics

 My manager has tasked me with providing summary statistics for each column. Specifically, they've asked for the average and median, along with the minimum and maximum values, for every individual column.

 ![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/4dcdc755-2311-4904-ac1f-c5b643ee6dbe)
 ![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/4673a943-18d1-40bb-85de-8d2b47cd20ed)

Exploring the data through basic measures like minimum, maximum, and average values provides an initial understanding of the dataset's range and central tendencies. While this approach may seem straightforward, it offers valuable insights into the variability and distribution of the variables. These summary statistics serve as a starting point for uncovering patterns and anomalies, setting the stage for more in-depth analyses.

## Investigating June 1

The most critical variable is the "% Iron Concentrate." However, our engineering colleague highlights the significance of the "% Silica Concentrate," "Ore Pulp pH," and "Flotation Column 05 Level" as well. 

Notably, the date is also of importance. Our supervisor has brought to our attention an anomaly on June 1, 2017, and has requested an investigation into this unusual occurrence.

Let's look into the date to find out!

To begin our analysis, we focused on examining the data for a specific date, June 1. Our goal was to investigate the relationships between key variables: '% Iron Concentrate', '% Silica Concentrate', 'Ore Pulp pH', and 'Flotation Column 05 Level'. These variables play a significant role in determining the quality of the iron ore concentrate. To achieve this, we first extracted the data for June 1 and then proceeded to visualize the relationships using scatter plots. By utilizing the sns.pairplot() function, we created a matrix of scatter plots that allowed us to visually assess the connections between these variables.This approach enabled us to gain a better understanding of potential correlations, patterns, and trends among the selected variables. This initial visualization served as a valuable starting point for identifying any noteworthy associations and laid the foundation for more in-depth correlation analysis.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/c678fa89-8bb7-43c5-8125-064a57a9b664)

**While the correlations are not highly significant, they do offer valuable insights into potential relationships among the variables.** The negative correlation between "% Iron Concentrate" and "% Silica Concentrate" aligns with expectations, indicating an inverse relationship. Additionally, weak correlations between "% Iron Concentrate" and other variables, such as "Ore Pulp pH" and "Flotation Column 05 Level," suggest possible influences but not strong linear associations. Similarly, the correlations involving "% Silica Concentrate," "Ore Pulp pH," and "Flotation Column 05 Level" provide insights into potential connections, although they are not very strong. Overall, these findings imply complex interactions within the iron ore concentration process that merit further exploration.

## Variation in Concentrations Throughout the Day

The identified correlations hint at intricate relationships within the iron ore concentration process that invite further investigation. My supervisor concurs and seeks a deeper understanding of the scenario.

What's our approach? Specifically, they are keen on visualizing the fluctuations in Concentrations over the course of the day. Yet, their interest extends to examining all columns. Therefore, crafting a graph would offer a valuable means to illustrate the outcomes effectively.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/19f1c49c-cebc-4dc7-abf1-a4d5e4e824c7)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/d4521f55-b3c7-49b1-9db8-7d855911e84f)

I noticed that there is a dip in concentrations for iron, while there is a rise for silica. So I wanted to plot it on the same axis to get a better view.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/f58bb329-69b5-4e5f-b342-1b9174d8ca69)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/7bcd91df-7185-4d09-a8d4-68057f589df7)

**The concurrent occurrence of a drop in iron concentration and an increase in silica concentration suggests potential challenges within the flotation plant's separation process.** This phenomenon could stem from issues related to flotation efficiency, chemical balance, equipment performance, or ore feed variability. Identifying the root cause requires a comprehensive analysis of process conditions, operational decisions, and data accuracy. Addressing these issues is crucial to maintaining the desired product quality and optimizing the overall flotation plant's performance.

To check if this is common or unusual, I looked at how iron and silica levels relate. I used a correlation number to see how strong their connection is and whether their opposite changes are typical or not.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/58711db1-78b6-445b-a1a4-f2fdf13962a3)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/e68027a3-45c9-460d-b5ca-7318f664967f)

**The correlation coefficient of -0.8005 between the concentrations of iron and silica reveals a notable pattern: as the iron concentration increases, the silica concentration tends to decrease, and vice versa This negative correlation aligns with our expectations, as higher iron content typically corresponds to lower silica content in the ore concentrate.** This relationship is integral to the mineral processing process, where the extraction and refinement of iron ore often involve the reduction of impurities like silica. Therefore, observing this inverse correlation reinforces the fundamental understanding of how these variables interact and impact the quality of the final iron product. 

# Comparing the Iron Concentration Per Month of June and July

My boss was interested in comparing the average iron concentration for the months of June and July, focusing on the distribution across different days of the week. To address this, I analyzed the dataset and extracted the iron concentration data for these two months. By calculating the average iron concentration for each day of the week, I was able to provide a clearer understanding of how iron concentration varies throughout the week. This comparison helps highlight any potential trends or patterns in iron concentration between the two months and sheds light on whether any significant differences exist in iron processing during these periods.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/a0be9a18-7ceb-449b-81a6-e53b7f6b40ff)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/ced0e1a5-ba97-493f-b29d-99f5b930f020)


Upon analyzing the data, a notable observation emerges regarding the average iron concentration for the months of June and July, specifically on Tuesdays. In the month of June, the average iron concentration on Tuesdays was 64.45, which was the lowest among all the days of the week for that month. This suggests a potential fluctuation or variation in iron concentration on Tuesdays in June. On the other hand, in July, the average iron concentration on Tuesdays was 64.35, also the lowest among the days of the week for that month. **Interestingly, the fluctuation in iron concentration on Tuesdays seems to persist in both months, although the overall range of fluctuation appeared to be more pronounced in June compared to July This indicates that the iron concentration experienced more variability on Tuesdays in June, whereas the fluctuations were relatively smaller on Tuesdays in July.** The rest of the days also show variations, with slight differences in average iron concentration between the two months.

# Any Monthly patterns in Iron Concentration?

In response to my boss's request for deeper insights into the iron concentration levels, a comprehensive analysis was conducted to explore potential trends across different months. The objective was to identify any patterns or noticeable changes in the average iron concentration.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/bcceb302-338f-4961-92ed-92d672a6c608)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/ef569d44-adca-4993-a29d-d0f9e8fe97ca)

Upon analyzing the data regarding iron concentration across different months, **it becomes evident that there is no discernible consistent pattern in the levels**. Instead, the iron concentration levels exhibit fluctuations that do not follow a specific trend. This observation suggests that various factors, including operational conditions and external influences, might contribute to the variability in iron concentration. Consequently, it's challenging to identify a clear trend or pattern in the data, and the levels appear to fluctuate without a consistent direction or correlation with the passage of time. This investigation underlines the complexity of the factors influencing iron concentration, as the absence of an identifiable pattern suggests that various dynamic variables contribute to the observed fluctuations. While the absence of distinct trends challenges the straightforward identification of correlations, this analysis provides valuable insights into the intricate nature of iron concentration levels and the potential factors influencing them.

## Key Findings Recap:

1. **Correlation Complexity:** The dataset's correlation matrix revealed moderate relationships between key variables, such as "% Iron Concentrate," "% Silica Concentrate," "Ore Pulp pH," and "Flotation Column 05 Level." While not strongly linear, these correlations provided a foundation for further investigation into potential associations.

2. **Concentration Dynamics:** Fluctuations in iron and silica concentrations throughout the day suggested challenges in the separation process. Identifying the causes of these fluctuations, whether from operational decisions or equipment performance, is pivotal for maintaining product quality and plant efficiency.

3. **Iron-Silica Relationship:** The inverse correlation between iron and silica concentrations, with a coefficient of -0.8005, aligned with expectations. This understanding reinforced the fundamental connection between iron's rise and silica's fall, essential for effective mineral processing.

4. **Monthly Insights (June and July):** A comparative analysis of iron concentrations on Tuesdays in June and July revealed consistent dips. While fluctuations persisted in both months, June showcased more pronounced variations, hinting at operational variations.

5. **Month-to-Month Variation:** Iron concentration across different months exhibited fluctuations without a clear pattern. This complexity underscored the role of multiple dynamic factors influencing iron concentration levels.

## Recommendations 

1. **Operational Optimization:** Investigate the reasons behind fluctuations in iron and silica concentrations throughout the day. Analyze operational decisions, equipment performance, and process conditions during these periods to improve process efficiency and product quality.

2. **Root Cause Analysis:** Address the variations in iron concentration observed on Tuesdays in June and July. Collaborate with experts to identify whether these variations stem from external factors, equipment issues, or other influences. This could lead to stabilizing iron concentration levels and enhancing process consistency.

3. **Collaboration and Knowledge Sharing:** Engage with domain experts, metallurgists, and engineers to gain deeper insights into the mining and mineral processing processes. Their expertise can provide valuable context and guide the analysis toward more actionable insights, ultimately contributing to process optimization.


You can view my code more in-depth [here](files/Metals.pdf).

## Thanks for reading!

I'm always on the lookout for data analyst opportunities. Know of any? Don't hesitate to reach out at [smitchellbest@gmail.com](mailto:smitchellbest@gmail.com). Make sure to explore more of my portfolio. Just click the button below.

<a href="javascript:history.back()" style="display: inline-block; padding: 10px 20px; background-color: #007bff; color: #fff; text-decoration: none; border-radius: 4px;">Go Back</a>

