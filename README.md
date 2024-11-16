# Canadian Cheese: An Excel Data Analysis Project

### Data Source
For this project, I used a dataset called the “Canadian Cheese Directory,” which I found on Kaggle, posted by Noah Janes. You can access the dataset via this [link](https://www.kaggle.com/datasets/noahjanes/canadian-cheese-directory). The dataset piqued my curiosity, making the analysis both engaging and a valuable learning experience.

### Objectives
- Clean and prepare the data for analysis.
- Utilize Pivot Tables and slicers to explore the data.
- Create an interactive dashboard for visualization.

### Tools
- Microsoft Excel

### Data Cleaning and Preparation
- The dataset was in a '.csv' format (comma-separated values), so I used Power Query to import and transform the data from a CSV file into an Excel file.

- I used the formula `=COUNTBLANK(cheese_data[CheeseID])` to check for any missing values.

- I added a new column next to 'ManufacturerProvCode' called 'ManufacturerProvName'. Using an IF function, I replaced the province abbreviations in 'ManufacturerProvCode' with their full names for clarity:

  ``` 
  =IF(B2="NB","New Brunswick",IF(B2="AB","Alberta",IF(B2="BC","British Columbia",IF(B2="MB","Manitoba",IF(B2="NL","Newfoundland and Labrador",IF(B2="NS","Nova Scotia",IF(B2="ON","Ontario",IF(B2="PE","Prince Edward Island",IF(B2="QC","Quebec",IF(B2="SK","Saskatchewan",""))))))))))
  ```

- I analyzed the 'MoisturePercent' column using Excel’s Data Analysis Tool to generate 'Descriptive Statistics'. Alternatively, the `AVERAGE` function can be used to calculate the mean of 'MoisturePercent'.

- I modified the 'Organic' column values using the 'Find and Replace' feature: replacing '0' with 'No' and '1' with 'Yes' for better readability, especially if the 'Organic' column is used as a slicer in the dashboard.

### Data Exploration

Exploratory Data Analysis (EDA) focused on answering several key questions:

- What is the most commonly used milk type in Canadian cheese production?
- Which are the top three cheese-producing provinces in Canada?
- What are the highest and lowest average moisture percentages in cheese, categorized by cheese type and fat content?

### References
- [The Importance of Data Analytics in Today's Business World](https://dataforest.ai/blog/the-importance-of-data-analytics-in-todays-business-world)
- [Clean Data from Excel, CSV, PDF, and Google Sheets with Data Interpreter](https://help.tableau.com/current/pro/desktop/en-us/data_interpreter.htm)
