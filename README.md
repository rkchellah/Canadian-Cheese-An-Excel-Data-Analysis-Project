# Canadian-Cheese-An-Excel-Data-Analysis-Project

### Data Source <br>
The dataset that I used for this project, is a dataset that I found on
Kaggle named “Canadian Cheese Directory” posted by Noah Janes [Download here](https://www.kaggle.com/datasets/noahjanes/canadian-cheese-directory) You can
find the data set by clicking at the embed link above. This spark a curiosity within me and making it more fun to work with. And it’s a chance to learn something new as well!

### Objectives
- Clean and prepare the data for analysis
- Use Pivot Tables and slicers to analyse the data
- Create an interactive dashboard for visualization
  
### Tools
- Microsoft Excel

### Data Cleaning/Preparation
- The format file of the data is a '.csv', a comma separated value. So I use Power Query to load the data, transforming it from a csv file to an excel file.

- Use the ``` =COUNTBLANK(cheese_data[CheeseID] ``` formula to check for any null values

- Created a new column beside to the 'ManufacturerProvCode' column and named it 'ManufacturerProvName', on this new column I used the if conditional function to create actual real    province names instead of usin the abbreviated ones in the 'ManufacturerProvCode' column

  ``` =IF(B2="NB","New Brunswick",IF(B2="AB","Alberta",IF(B2="BC","British Columbia",IF(B2="MB","Manitoba",IF(B2="NL","Newfoundland and Labrador",IF(B2="NS","Nova  Scotia",IF(B2="ON","Ontario",IF(B2="PE","Prince Edward Island",IF(B2="QC","Quebec",IF(B2="SK","Saskatchewan","")))))))))) ``` Thus creating this

- Selected the MoisturePercent column and used the data analysis to find the ‘Descriptive Statistics’. Note: You can also use the AVG (average) excel function to find the mean of
 ‘MoisturePercent’.   

- Changing the Organic Value, By using the ‘Find and Replace’ method just like before, We can replace ‘0’ into a ‘No’ and ‘1’ into a ‘Yes’. Considering it is easier to understand  ‘Yes’ and ‘No’ rather than ‘0’ and ‘1’. And it will be better considering we might using
the ‘Organic’ column as a slicer in the future.

### Data Exploration

EDA involved exploring the data to answer key questions, such as:

- What is the most commonly used milk type for cheese production in Canada?
- What are the top three cheese-producing varieties provinces in Canada?
- What are the highest and lowest average moisture percentages in cheese, categorized by cheese type and fat level?

### References

- The Importance of Data Analytics in Today's Business World https://dataforest.ai/blog/the-importance-of-data-analytics-in-todays-business-world
- Clean Data from Excel, CSV, PDF, and Google Sheets with Data Interpreter https://help.tableau.com/current/pro/desktop/en-us/data_interpreter.htm

