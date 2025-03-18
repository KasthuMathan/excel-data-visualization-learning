# data-visualization-learning
 Excel Data Visualization is done with the help of Alex Freberg's tutorial.
 
## Project Overview
- This project focuses on data cleaning, analysis, and visualization in Excel.
- The dataset contains customer details, include income, age, commute distance, and bike purchase status.

## Dataset
- The dataset used in this project is the same dataset from Alex Freberg's tutorial.
- To follow along, you can check it on his channel [here](https://www.youtube.com/@AlexTheAnalyst).

## 1. Data Cleaning
### 1. Removed Duplicates
- Used **Data > Data Tools > Remove Duplicates** to clean duplicate records.

### 2. Replaced Categorial Values
- Marital Status:
  - M -> Married
  - S -> Single

- Gender:
  - F -> Female
  - M -> Male

### 3. Corrected Spelling Errors
- "Management" -> "Maleanagement"
- "Manual" -> "Maleanual"
- "Skilled Manual" -> "Skilled Maleanual"
- "Miles" -> "Maleiles"
- These errors occurred when replacing M with Male, causing unwanted changes.

### 4. Created Age Brackets
- The dataset contains ages from 25 to 89, making analysis difficult.
- Used the following **IF** formula to categorize:

```excel
=IF(L2>54,"Old 55+",IF(L2>=31,"Middle Age 31-54",IF(L2<31,"Adolescent 0-30","Invalid")))
```

## 2. Pivot Tables
### Average Income Analysis
1. Created a Pivot Table (Selected the whole table)
![images/1. Average Income.png](https://github.com/KasthuMathan/excel-data-visualization-learning/blob/main/images/1.%20Average%20Income.png)

3. Added:
  - Income -> Values (Changed Sum to Average)
  - Gender -> Rows
  - Purchased Bike -> Columns
3. Chart type: 2D Clustered Column Chart
![images/2. Average Icome Chart.png](https://github.com/KasthuMathan/excel-data-visualization-learning/blob/main/images/2.%20Average%20Icome%20Chart.png)

### Commute Distance Analysis
1. Created a Pivot Table with:
  - Commute Distance -> Rows
  - Bike Purchase -> Values (Count of Purchases)
  - Bike Purchase -> Columns
![images/3. Commute Distance.png](https://github.com/KasthuMathan/excel-data-visualization-learning/blob/main/images/3.%20Commute%20Distance.png)
2. Chart type: 2D Line Chart
![images/4. Commute Distance Chart.png](https://github.com/KasthuMathan/excel-data-visualization-learning/blob/main/images/4.%20Commute%20Distance%20Chart.png)

## 3. Age Brackets Analysis
1. Created a Pivot Table with:
  - Age Brackets -> Rows
  - Bike Purchase -> Values (Count of Purchases)
  - Bike Purchase -> Columns
![images/5. Age Brackets.png](https://github.com/KasthuMathan/excel-data-visualization-learning/blob/main/images/5.%20Age%20Brackets.png)
2. Using Age Brackets makes analysis clearer compared to raw age values.
### Age Bracket
![images/6. Age Brackets Chart.png](https://github.com/KasthuMathan/excel-data-visualization-learning/blob/main/images/6.%20Age%20Brackets%20Chart.png)

### Raw "Age"
![images/8. Ages Charts.png](https://github.com/KasthuMathan/excel-data-visualization-learning/blob/main/images/8.%20Ages%20Charts.png)
This raw "age" would be more complicated to identify and undersatnd clearly, so using an "Age Bracket" would make more clear by showing the age category.

## Dashboard
### Dashboard Elements
Included visualizations for:
  - Average Income Per Purchase
  - Customer Commute Distance
  - Customer Age Brackets

### Adding Filters (Slicers)
1. Go to **Pivot Chart Analyze > Insert Slicer**.
2. Selected filters:
  - Marital Status
  - Region
  - Education
3. Connected slicers to all Pivot Tables using:
  - Slicer > Report Connections
![images/9. Dashboard Visualization.png](https://github.com/KasthuMathan/excel-data-visualization-learning/blob/main/images/9.%20Dashboard%20Visualization.png)

Now, the dashboard dynamically filters data for deeper insights.

## Conclusion
By cleaning data, structuring pivot tables, and designing a dashboard, we created interactive and insightful visualizations to analyze bike purchases.

## Credits
This project follows the Excel Data Visualization tutorial by **Alex Freberg**.