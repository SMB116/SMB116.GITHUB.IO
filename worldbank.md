# Dominica's Financial Journey: Funds, Debts, and Resilience Projects

I have always wanted to visit the breathtaking island of Dominica, especially since my dad told me that his mother is originally from there. Now, I know what you're thinking, but no, it's not the Dominican Republic, as it's often confused to be. While the Dominican Republic is known for its superstar baseball players, beautiful tourist resorts, and amazing nightlife, Dominica is a small island known as the natural gem of the Caribbean. With its lush rainforests, hidden waterfalls, and pristine beaches, Dominica offers a serene and unspoiled retreat where native culture is preserved, and nature is treasured. However, even with such natural beauty, financially, it's a different story. Dominica is one of the less economically developed islands in the Caribbean region. It faces various challenges in terms of economic growth, infrastructure development, limited natural resources, and the risk of natural disasters. All of these factors contribute to its classification as one of the poorer islands in the Caribbean.

To explore Dominica's economic development and financial progress, it is best to look at the World Bank for information on the country's financial assistance and projects. The World Bank is an international financial institution that offers financial and technical assistance to developing countries. It aims to reduce poverty, promote economic development, and improve living conditions. The World Bank provides support to over 100 countries globally, including Dominica. Through financial resources, technical expertise, and advisory services, the World Bank helps Dominica address challenges in economic development, infrastructure, and disaster recovery, fostering sustainable growth and improved livelihoods.

## Inquiry Questions:

1. How many transactions are due?
2. How much money was given to Dominica from the IDA?
3. How much money was repaid by Dominica?
4. How much money is owed by Dominica?
5. What is the maximum amount owed by Dominica?
6. What are the top three projects owed by Dominica?

I downloaded the live dataset from the World Bank website to obtain a present-day picture of Dominica's relationship with the World Bank. (You can access and download the dataset [here](https://finances.worldbank.org/Loans-and-Credits/IDA-Statement-Of-Credits-and-Grants-Historical-Dat/tdwh-3krx), as it updates frequently.) The dataset I used was last uploaded on July 10, 2023.

Given that the dataset contained 1.19 million rows and 30 columns of data, I decided to use SQL to answer the inquiry questions. For this project, I used the website [CSVFiddle.io](https://csvfiddle.io), an online platform for working with CSV files. I utilized this tool to perform SQL queries on CSV data in a user-friendly and interactive environment. The platform allowed me to upload, edit, and manipulate CSV data directly in the browser. With real-time previews, I could visualize the impact of my SQL queries on the data and explore the results efficiently. This made it convenient to interact with and analyze CSV data without the need for complex setups or installations.

Using the following SQL commands:

```sql
SELECT | FROM | WHERE | DISTINCT | AS | GROUP BY | MAX | ORDER BY | LIMIT
```

## Key Insights:

- **Given Funds:** Dominica has received a substantial amount of $17 billion USD from a funding source.
- **Repaid Debt:** Dominica has paid $1.27 billion to the World Bank.
- **Debt Owed:** Dominica currently owes $645 million USD to the International Development Association (IDA).
- **Largest Debt:** Dominica's largest outstanding debt is $30 million USD, which is related to COVID-19 response and recovery projects.
- **COVID-19 Projects:** The top two projects that Dominica owes are all related to COVID-19.
- **Hurricane Maria Projects:** Curiously, projects unrelated to COVID-19 were connected to Hurricane Maria, which struck Dominica in 2017.

## Let's begin exploration:

### Dominica's Transaction Tally

To kickstart our investigation into Dominica, I wanted to see how many transactions the World Bank had with Dominica to determine if there was enough data for evaluation.

<img src="images/Transactions.jpg?raw=true"/>

By utilizing the `COUNT` function and filtering the data to include only transactions related to Dominica, it was revealed that there were 2,730 transactions. It emphasizes that there is a substantial amount of data available for a thorough assessment of the country's financial dealings and development projects with the institution.

### Dominica's Receipts and Repayments

Next, I wanted to determine the amount of money that was approved and committed to action by the World Bank. Using the `SUM` function, I was able to combine all the amounts together, regardless of their status.

<img src="images/Given and Repaid.jpg?raw=true"/>

The data reveals that $17,205,735,200 USD was extended to Dominica from the World Bank. That's a lot of money! It surpasses my expectations, but considering Dominica's vulnerability to natural disasters due to its location, it's understandable that they would receive such a significant amount.

Seeing such a large number had me curious about how much the country had paid back. With similar queries, but just changing the column in question, I was able to retrieve the necessary information. Upon analysis, we learned that they have repaid the World Bank $1.27 billion of their debts. Therefore, approximately 7.38% of the money received has been paid back, revealing ongoing financial obligations and the necessity for continued support.

### Debt in Focus: Dominica's Financial Obligations

It made me wonder, how much do they owe currently? The dataset mentioned that money is owed to the IDA, and upon further research, I discovered that the IDA stands for the International Development Association. The International Development Association (IDA) is an arm of the World Bank Group that provides financial support and concessional loans to the world's poorest countries, allowing them to undertake development projects and initiatives to reduce poverty and promote economic growth.

<img src="images/debts.jpg?raw=true"/>

With a straightforward SQL query, I discovered that they owe the IDA $645,143,805.62 USD. The current owed amount, approximately 3.75% of the initial funding received ($17 billion), indicates a relatively low level of debt in proportion to the total amount provided by the IDA.

Curiously, I wanted to know the highest owed debt. Using the `MAX` function, I discovered that the maximum debt was only $30 million.

### Project Expenses: Dominica's Top Three High-Cost Projects

What could a country need $30 million dollars for? This led me to investigate and find out the details of the project.

<img src="images/Three top projects.jpg?raw=true"/>

Upon investigation, it became apparent that the top two highest cost projects for the country were all related to COVID-19, which was understandable given the pandemic's widespread effects. Both the Second COVID-19 Response & Recovery Program and the First COVID-19 Response & Recovery Program in Dominica have common goals. They both want to save lives, protect jobs, and preserve livelihoods during the pandemic. Additionally, they aim to strengthen fiscal policies for a resilient recovery. They're all about making the country stronger and better equipped to handle future challenges.

The third project, Third Phase Disaster Vulnerability Reduction Adaptable Program Loan, aimed to reduce vulnerability to natural hazards and climate change impacts in Dominica, which is especially crucial due to its hurricane-prone location in the Caribbean. Approved in 2014 and ending in 2020, the project focused on investing in resilient infrastructure and improving hazard data collection and monitoring systems. 

<img src="images/Graph.jpg?raw=true"/>

However, it faced challenges after Hurricane Maria struck in 2017, prompting adjustments to prioritize post-disaster recovery and rebuilding resilient infrastructure. Despite this setback, the project continued to strengthen Dominica's resilience against natural disasters and climate change impacts.

## Recap of Findings:

Dominica has received a substantial amount of $17 billion USD as funds. Currently, they owe $645 million USD to the International Development Association (IDA), but they have already repaid $1.27 billion to the World Bank. The largest outstanding debt of $30 million USD is related to COVID-19 response and recovery projects. Interestingly, Dominica's top two projects are focused on addressing the impact of COVID-19, while the third project deals with natural hazards and climate change, like Hurricane Maria, which struck the country in 2017.
