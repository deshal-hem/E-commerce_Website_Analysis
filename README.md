# E-commerce Website Analysis

<img width="975" height="545" alt="image" src="https://github.com/user-attachments/assets/96af067e-d555-4abd-9b70-b265a90ccb5a" />

## Objective
The goal was to analyze an e-commerce platform’s performance using data on website traffic, marketing spend, customer activity, and revenue. The analysis focused on understanding customer behavior, evaluating marketing effectiveness, and assessing sales performance to generate insights that support data-driven decision-making for strategic use.

## Link to Dashboard
https://app.powerbi.com/view?r=eyJrIjoiYzQ5OGMyMWQtMjM0OS00ODIxLWI0OTAtYzNiMzU5ZDE4MmJmIiwidCI6IjFkYTQ1MTA3LTFmNTMtNGE4MC1iNTMzLTliMTg4Nzk2MGNlOSIsImMiOjEwfQ%3D%3D&pageName=928125f84e38faa74eaf

## Further Information
Python was used to conduct the analysis in a Jupyter Notebook environment, enabling an organized workflow that comprised exploratory analysis, feature engineering, data cleaning, and preliminary visualization. Power BI was used to generate the final dashboard.

Importing essential libraries like Matplotlib for visualization and Pandas and NumPy for data handling was the first step. Next, the dataset was loaded into a Pandas DataFrame.

A quick examination with .head() and .info() provided a summary of the data structure. This showed that although the information was reasonably comprehensive, null (missing) values were present in a number of columns, including those for revenue, purchases, and marketing spend. Consequently, the following data cleaning techniques were used:

  • All column headers were converted to lower case to ensure consistency during the Python data exploration stage.
  • The data type of the date column was changed to datetime.
  • Rows with null values were not removed as they accounted for a significant portion of the data set (27%). Instead, all null values were replaced with the median of the respective columns.
  • The day of week information was extracted from the date column and named as Day Name.
  
Once the data the was cleaned, it was exported as a csv file which was then used in Power BI to create a final dashboard.

Further minor adjustments were made to the dataset while creating the dashboard in Power BI:
  • Column headers were now renamed to a user-friendly format.
  • Data types for Cart Abandonment Rate, Conversion Rate and Repeat Purchase Rate were converted from decimals to percentages.
  • The first 3 characters of the Day Name column was extracted for simplicity.
  
Afterwards, various measures, such as Total Revenue, Total Visitors, Avg Conversion Rate and Avg Cart Abandonment Rate were created to aggregate the data. Some new measures such as Avg Order Value and Avg ROAS (explained later) were also created that were not part of the initial dataset.

Various charts, like column charts, pie charts, line charts and bar charts were then created with the help of these newly created measures.

## Key Insights
From the analysis, several important findings emerged:
  • Marketing Efficiency: Certain campaigns such as Holiday Offers generated more revenue for the money spent ($2.32 for every $1 spent on marketing) compared to others like Weekend Discount ($1.92 for every $1 spent on marketing)
  • Customer Segment: New customers tend to bring in more visits, purchases and revenue while maintaining a better conversion rate compared to returning customers.
  • Traffic Timing: People tend to visit the website more on certain days of the week than others. For instance, Tuesday had the highest avg visits (1,169), followed by Thursday (1,159). Friday had the lowest website traffic (996).
  • Organic search, while having the highest repeat purchase rate (19.1%), had the highest cart abandonment rate as well (31.1%). This indicates that a portion of organic visitors maybe facing certain challenges that prevent them from checking out.
