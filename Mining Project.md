# Mining Project 
### By Shekela Mitchell Best

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

While the correlations are not highly significant, they do offer valuable insights into potential relationships among the variables. The negative correlation between "% Iron Concentrate" and "% Silica Concentrate" aligns with expectations, indicating an inverse relationship. Additionally, weak correlations between "% Iron Concentrate" and other variables, such as "Ore Pulp pH" and "Flotation Column 05 Level," suggest possible influences but not strong linear associations. Similarly, the correlations involving "% Silica Concentrate," "Ore Pulp pH," and "Flotation Column 05 Level" provide insights into potential connections, although they are not very strong. Overall, these findings imply complex interactions within the iron ore concentration process that merit further exploration.

## Variation in Concentrations Throughout the Day

The identified correlations hint at intricate relationships within the iron ore concentration process that invite further investigation. My supervisor concurs and seeks a deeper understanding of the scenario.

What's our approach? Specifically, they are keen on visualizing the fluctuations in Concentrations over the course of the day. Yet, their interest extends to examining all columns. Therefore, crafting a graph would offer a valuable means to illustrate the outcomes effectively.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/19f1c49c-cebc-4dc7-abf1-a4d5e4e824c7)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/d4521f55-b3c7-49b1-9db8-7d855911e84f)

I noticed that there is a dip in concentrations for iron, while there is a rise for silica. So I wanted to plot it on the same axis to get a better view.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/f58bb329-69b5-4e5f-b342-1b9174d8ca69)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/7bcd91df-7185-4d09-a8d4-68057f589df7)

The concurrent occurrence of a drop in iron concentration and an increase in silica concentration suggests potential challenges within the flotation plant's separation process. This phenomenon could stem from issues related to flotation efficiency, chemical balance, equipment performance, or ore feed variability. Identifying the root cause requires a comprehensive analysis of process conditions, operational decisions, and data accuracy. Addressing these issues is crucial to maintaining the desired product quality and optimizing the overall flotation plant's performance.

To check if this is common or unusual, I looked at how iron and silica levels relate. I used a correlation number to see how strong their connection is and whether their opposite changes are typical or not.

![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/58711db1-78b6-445b-a1a4-f2fdf13962a3)
![image](https://github.com/SMB116/SMB116.GITHUB.IO/assets/124625985/e68027a3-45c9-460d-b5ca-7318f664967f)

The correlation coefficient of -0.8005 between the concentrations of iron and silica reveals a notable pattern: as the iron concentration increases, the silica concentration tends to decrease, and vice versa. This negative correlation aligns with our expectations, as higher iron content typically corresponds to lower silica content in the ore concentrate. This relationship is integral to the mineral processing process, where the extraction and refinement of iron ore often involve the reduction of impurities like silica. Therefore, observing this inverse correlation reinforces the fundamental understanding of how these variables interact and impact the quality of the final iron product. 








