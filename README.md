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
![images/1. Average Income]<img width="743" alt="Image" src="https://github.com/user-attachments/assets/5231a0ec-1330-4f3f-9eab-96023a45e5d5" />
2. Added:
  - Income -> Values (Changed Sum to Average)
  - Gender -> Rows
  - Purchased Bike -> Columns
3. Chart type: 2D Clustered Column Chart

### Commute Distance Analysis
1. Created a Pivot Table with:
  - Commute Distance -> Rows
  - Bike Purchase -> Values (Count of Purchases)
  - Bike Purchase -> Columns
2. Chart type: 2D Line Chart

## 3. Age Brackets Analysis
1. Created a Pivot Table with:
  - Age Brackets -> Rows
  - Bike Purchase -> Values (Count of Purchases)
  - Bike Purchase -> Columns
2. Using Age Brackets makes analysis clearer compared to raw age values.

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
  -Slicer > Report Connections

Now, the dashboard dynamically filters data for deeper insights.

## Conclusion
By cleaning data, structuring pivot tables, and designing a dashboard, we created interactive and insightful visualizations to analyze bike purchases.

## Credits
This project follows the Excel Data Visualization tutorial by **Alex Freberg**.