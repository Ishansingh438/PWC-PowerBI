# PWC-PowerBI

![image](https://github.com/Ishansingh438/PWC-PowerBI/assets/105629591/9ce25454-1d15-4e4c-b798-0066fe4dee22)

                                                                       
Problem Statement :
In this project Create a dashboard in Power BI for the call center manager that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset.

Possible KPIs include (but not limited to):

Overall customer satisfaction
Overall calls answered/abandoned
Calls by time
Average speed of answer
Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

🔍 Project Highlights:

✅ Data Visualization: I transformed raw telecom data into actionable insights by creating visually appealing charts, graphs, and reports.


📈 KPI Focus: The dashboard focuses on crucial KPIs such as customer satisfaction, call metrics, and agent performance to guide strategic decision-making.


🎨 Interactive Design: Users can filter and slice data, allowing for a dynamic exploration of telecom trends.


🔐 Data Security: I ensured data security and privacy compliance throughout the project.


🌐 Cross-Platform Access: The dashboard is accessible on Power BI Service for easy sharing and collaboration.


Project Goal :- 
To help our client gain valuable insights into customer preferences and key performance indicators (KPIs).

Create a dashboard in Power BI for Claire that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset.

Data Analysis (DAX):

Measures used in all visualization are:

Average of seed of answerd = AVERAGE('call centre trends'[Speed of answer in seconds])

Average of statisfaction = AVERAGE('call centre trends'[Satisfaction rating])

Count satisfation rating = COUNT('call centre trends'[Satisfaction rating])

Overall Customer Satisfation = DIVIDE([Possitive satisfation rating],[Count satisfation rating],0)

Possitive satisfation rating = CALCULATE(COUNT('call centre trends'[Satisfaction rating]),FILTER('call centre trends','call centre trends'[Satisfaction rating] IN {4,5}))

resolved calls = COUNTX(FILTER('call centre trends','call centre trends'[Resolved] = "Yes"), 'call centre trends'[Resolved])

Unresolved calls = COUNTX(FILTER('call centre trends','call centre trends'[Resolved] = "No"), 'call centre trends'[Resolved])

total calls = CALCULATE('Table'[total calls answered] + 'Table'[total calls unanswred])

total calls answered = COUNTX(FILTER('call centre trends','call centre trends'[Answered (Y/N)] = "Yes"),'call centre trends'[Answered (Y/N)])

total calls unanswred =COUNTX(FILTER('call centre trends','call centre trends'[Answered (Y/N)] = "No"), 'call centre trends'[Answered (Y/N)])

Insights :
As shown by Data Visualization, It can be deduced that:

Most of the satisfaction ratings from each call are 3 and 4.
The average satisfaction rating has decreased over the span of three months. January brought the highest satisfaction rating and march the lowest.
The percentage of issue resolved in January was the highest, with a dip in February. It increased again in march.
The majority of calls come in the morning.
The average speed of answer by Joe is the highest.
The call resolution rate of Jim is the highest, even though the average speed of his answers is lower compared to those of Joe, Martha and Dan. The call answered by - him are also higher than the average number of calls answered.
Becky's speed of answer is the lowest among all, and her rate of calls resolved is higher. She is in the 5th position in the call resolution rate.
Martha has the highest speed of answered in the sec

                                                                        Customer Retention

I'm excited about the impact this project will have on our client's operations and their ability to better serve their customers.
