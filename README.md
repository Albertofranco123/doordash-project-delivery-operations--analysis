# DoorDash Delivery Operations Analysis – Power BI Project

This project analyzes DoorDash-style pizza delivery performance using descriptive, diagnostic, and predictive analytics in Power BI.

---

DoorDash Delivery Analysis – SOAR Report
1. S — Specify (Problem Definition)

The objective of this analysis is to evaluate delivery performance across multiple restaurants in a DoorDash-style delivery environment. The project focuses on understanding:

Why delivery orders arrive late

What factors in the dataset contribute to delivery delays

Which types of orders are more likely to experience delays

How to reduce the average delivery delay

How many orders can be expected in the next two years based on forecasting

These questions align with the following analytical perspectives:

Descriptive: What is the overall delivery performance?

Diagnostic: Why do delays occur, and what factors explain failures?

Predictive: How will order volume behave over the next two years?

2. O — Obtain (Data Collection & Preparation)

Dataset Source:
https://www.kaggle.com/datasets/akshaygaikwad448/pizza-delivery-data-with-enhanced-features/data

Data preparation was performed in Power BI Desktop using Power Query.

Preparation steps included:

Correcting data entry errors, such as fixing the typo in “Marco’s Pizza” vs “Marcos Pizza” using Replace Values

Formatting columns with the correct data types (dates, decimals, whole numbers)

Creating a binary column that converted the Is_Delayed TRUE/FALSE values into 1/0 to simplify DAX calculations using COUNT

These data cleaning steps ensured accurate measures and reliable visualizations for the analysis.

3. A — Analyze

The analysis is divided into Descriptive, Diagnostic, and Predictive sections.

Descriptive Analysis

Key KPIs:

Average Delivery Time: 29.49 minutes

Total Deliveries: 1004

Successful Deliveries: 794

Delivery Success Rate: 79.1%

Unsuccessful Deliveries: 20.9%

Descriptive Findings:

Delivery delays increase significantly during high-traffic hours, especially between 6:00 PM and 8:00 PM

Cities with the highest number of late deliveries include Boston, Los Angeles, Miami, Phoenix, and Seattle

Some restaurants have higher delay counts, with Papa John’s and Domino’s showing the most late orders

These metrics establish the baseline performance and highlight areas that require further examination.

Diagnostic Analysis

Traffic Impact on Delays:
Higher traffic levels show a clear correlation with increased delivery delay minutes. Restaurants in areas with Traffic Level 2–3 consistently experience longer delays.

Pizza Complexity:
Higher ingredient complexity leads to increased failure rates (late or unsuccessful deliveries).
Success rates drop significantly once pizza complexity exceeds 12–15 ingredients.
Simple pizzas tend to have better performance, while highly complex pizzas carry a higher delay risk.

Restaurant Performance Variability:
Some restaurants are more affected by traffic and complexity than others, indicating operational inefficiencies.
Papa John’s and Domino’s show higher delay counts, potentially due to longer prep times, higher order volume, or inadequate scheduling during peak periods.

Predictive Analysis

Forecasting was performed using a time-series visualization of Total Orders Over Time for the next two years.

Historical order volume starts low and stable, then gradually increases.
The forecast shows continued growth, suggesting increasing demand in future periods.

4. R — Report (Insights & Recommendations)
Insights

Traffic and the number of pizza ingredients (complexity) are strong predictors of delivery delays

On average, restaurants show similar percentages of delays

Improving the success rate requires preparing ingredients in advance during peak hours to reduce cooking and assembly times

Delivery logistics and driver coordination must be improved, as traffic plays a major role in delays

Key Calculations

Avg Time per KM:
Calculated as the SUM of all delivery durations in minutes divided by the SUM of all distance in kilometers.
This metric improves accuracy because it incorporates distance as a variable.

Delay Rate:
Count all orders where Is_Delayed = TRUE.

Delivery Success and Failure Rates:

Failure Rate = Late Deliveries / Total Orders

Success Rate = Orders Delivered On Time / Total Orders

## 📂 Files in This Repository

| File | Description |
|------|-------------|
| `Dashboard_Analysis.pdf` | Main analysis report using the SOAR framework |
| `Executive_summary_Doordash_project.docx` | Executive summary (Word version) |
| `Executive_summary_Doordash_project.pdf` | Executive summary (PDF version) |
| `Proyect_DoorDash_OPS_Analysis_AlbertoFranco.pbix` | Power BI dashboard file |
| `README.md` | Project documentation |

---

## 📧 Author
**Alberto Franco**  
Data Analytics & Operations Projects
