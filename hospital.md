# I'm sorry to tell you, but here's the data: Insights into Hospital Practices

Where is the place where tears of joy are formed when the first sounds of life are taken, and tears of grief flow when the final breath is drawn?

<div style="text-align: center;">
<img src="images/thinking.gif?raw=true"/>
</div>

That's right—the hospital.

Regardless of your feelings, a hospital is what is needed in society, serving as the cornerstone of healthcare and the backbone to support others.

In my role as a data analyst in the healthcare sector, I report to the data manager of our department. As you can imagine, working in a hospital setting, my boss consistently swaps between numerous responsibilities and has entrusted me with the crucial task of investigating specific data-related matters.

This responsibility is vital to ensure that hospital operations run smoothly and efficiently, and that informed, data-driven decisions are made to enhance patient care and overall healthcare outcomes.

**Business questions:**

1. What does the distribution of time spent in the hospital look like? Specifically, are the majority of patients staying for less than 7 days?
2. What is the average number of procedures performed by different medical specialties in the hospital?
3. Does the hospital exhibit any disparities in the treatment of patients from different races, particularly concerning the number of lab procedures performed?
4. Is there a correlation between the number of lab procedures and the length of hospital stay?

The dataset being utilized encompasses a decade's worth (1999-2008) of clinical care data from 130 US hospitals and integrated delivery networks. It comprises more than 50 features, which capture patient and hospital outcomes. You can access the dataset [here](link_to_dataset).

To address the business problems, I leveraged MySQL Workbench to perform queries and extract valuable insights from the dataset.

To tackle the problems at hand, I employed various SQL querying techniques such as `RPAD` to generate a histogram, `GROUP BY`, `HAVING`, `DISTINCT`, `JOINS`, `CASE WHEN`, and Common Table Expressions (CTEs) to derive valuable insights from the dataset.

Each of these methods played a crucial role in transforming and analyzing the data, allowing me to efficiently address the business challenges and provide comprehensive solutions using SQL queries.

**Key Insight:**

Approximately 84% of patients are discharged within a week, highlighting the significant impact of hospital stay durations on operational efficiency.

The specialties "Surgery - Cardiovascular/Thoracic," "Surgery - Thoracic," and "Radiologist" have the highest average procedures, with a shared focus on diagnosing and treating cardiovascular conditions, and the latter two specializing in medical imaging expertise.

No significant gaps observed in average procedures between racial/ethnic groups; African Americans have the highest average. Further investigation is needed to ensure equitable healthcare practices.

A positive correlation exists between longer hospital stays and higher lab procedures, emphasizing the connection between both factors.

## The Analysis

### Analyzing Hospital Stay Distribution: Are patients staying longer than a week?

As a healthcare data analyst, my goal is to understand the distribution of time spent by patients in the hospital. This information is crucial for optimizing hospital operations and resource allocation.

With limited beds available, it is essential to know how long patients typically stay to ensure efficient patient care and bed utilization.

By utilizing SQL queries, including the `RPAD` function, I aimed to generate a histogram and gain valuable insights into the distributions of the data. I'm particularly interested in identifying if the majority of patients stay less than 7 days, as this could help in prioritizing acute cases and streamlining the discharge process to free up beds promptly.

These findings will be instrumental in making data-driven decisions that benefit both patient care and the hospital's financial well-being.

<img src="images/histogram.jpg?raw=true"/>

With approximately 84% of patients discharged within a week, and an average hospital stay of 4 days, the high turnover rate emphasizes the success of efficiently managing hospital stay durations.

This finding underscores the considerable influence of these durations on operations, making it crucial to optimize resource allocation and patient care strategies.

### Analyzing Procedure Counts by Medical Specialties: Identifying High-Performing Departments

The new Hospital Director seeks to identify medical specialties that perform the highest number of procedures on average.

To fulfill this request, I utilized the SQL `GROUP BY` and `HAVING` clauses to obtain a list of all specialties along with their corresponding average total of procedures.

This allows the Director to efficiently analyze the data and make informed decisions regarding resource allocation and cost management in the hospital.

<img src="images/Top 3 Specialties.jpg?raw=true"/>

Among the medical specialties, "Surgery - Cardiovascular/Thoracic," "Surgery - Thoracic," and "Radiologist" stand out as having the highest average number of procedures.

These specialties primarily focus on diagnosing and treating cardiovascular conditions, with the latter two involving expertise in medical imaging techniques. In other words, these three specialties perform a significant number of procedures related to cardiovascular care, showcasing their expertise and importance in the hospital's medical services.

### Analyzing Racial Disparities in Lab Procedures: Does Race Matter?

The Chief of Nursing is interested in investigating whether the hospital's treatment of patients from different racial backgrounds varies, particularly concerning the number of lab procedures conducted.

To address this, I employed SQL queries utilizing the `AVERAGE` function, `GROUP BY` clause, and table joins. By grouping the data based on patient race and joining relevant tables, I was able to calculate the average number of lab procedures performed for each racial group.

This analysis allowed us to determine if there are any significant differences in the treatment received by patients from different racial backgrounds regarding the utilization of lab procedures.

<img src="images/race.jpg?raw=true"/>

The analysis reveals that, on average, there are no significant gaps observed in the number of procedures performed among different racial and ethnic groups.

Interestingly, African Americans show the highest average number of procedures among the groups studied.

However, it's important to approach these findings with caution, as they do not necessarily imply equitable healthcare.

Further investigation is necessary to understand the underlying factors contributing to these trends and to ensure that all patients receive fair and equitable access to healthcare services, regardless of their racial or ethnic backgrounds.

The data indicates a potential disparity in the number of procedures for African Americans, but a more comprehensive examination is essential to address any systemic biases and ensure healthcare equality for all patients.

### Analyzing the Relationship between Lab Procedures and Hospital Stay Length: Is there a correlation?

My boss is interested in understanding the potential correlation between the number of lab procedures and the length of hospital stays. They want to explore whether patients who undergo a higher number of lab procedures tend to stay in the hospital for a longer duration.

To address this question, I utilized the `CASE` statement to create bins and categorize patients based on the number of lab procedures they receive.

This approach allows us to analyze how the length of hospital stays varies across different categories of patients based on the number of lab procedures they undergo.

By examining these patterns, we can uncover valuable insights and determine if there is any association between the number of lab procedures and the length of hospital stays.

<img src="images/Hospital Stay vs Lab Procedures.jpg?raw=true"/>

Longer hospital stays and higher lab procedures exhibit a positive correlation, suggesting that patients with extended hospital stays tend to undergo more lab procedures. This insight can help optimize resource allocation and improve patient care planning, but further investigation is needed to understand the underlying factors contributing to this association.

### Highlighting Hospital Success Stories: Emergency Patients with Remarkably Short Stays

Lastly, the Hospital Administrator aims to showcase the hospital's most significant success stories, particularly focusing on cases where patients arrived in emergency situations but had shorter hospital stays compared to the average.

To find these success stories, I utilized a Common Table Expression (CTE) in my query. The CTE allowed me to efficiently filter and analyze the data, identifying patients who came in with emergencies and then determining if their hospital stays were below the average.

This approach helped highlight specific instances of successful emergency care, providing valuable insights for the Administrator to celebrate and replicate these positive outcomes.

<img src="images/Success stories .jpg?raw=true"/>

## Recap of Key Takeaways:

1. Hospital stays significantly influence operational efficiency, with approximately 84% of patients being discharged within a week.

2. Specialties like "Surgery - Cardiovascular/Thoracic," "Surgery - Thoracic," and "Radiologist" lead in average procedures, focusing on cardiovascular care and medical imaging.

3. There are no significant gaps in average procedures among racial/ethnic groups, but further investigation is needed to ensure equitable healthcare.

4. A positive correlation exists between longer hospital stays and higher lab procedures, indicating a connection between both factors.

<a href="javascript:history.back()" style="display: inline-block; padding: 10px 20px; background-color: #007bff; color: #fff; text-decoration: none; border-radius: 4px;">Go Back</a>

