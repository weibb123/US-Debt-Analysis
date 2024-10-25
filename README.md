# Content
- [Problem Statement](#Problem-Statement)
- [Question 1](#Question-1)
- [Question 2](#Question-2)
- [Question 3](#Question-3)
- [Final Findings](#Final-Findings)

## Problem Statement

You were hired by a small debt agency in Washington DC that specializes in analyzing and forecasting public and private debt.
The US Governement has requested an analysis of their public and governemental debt to answer some specific questions below.

Using the Questions and Data Dictionary Provided, answer the questions using charts/graphs and narratives.

### 3 Questions to answer

What was the Yearly Debt Percentage Increase for each year compared to the previous year?

Which months historically have seen the highest/lowest increases in Total debt?

What is the projected growth of the publicly held debt in the next few years?

### STEP 1:

![image](https://github.com/user-attachments/assets/2952e675-a119-4633-a1c5-ce7fe899f64a)

initial dataset looks like this with about 7000 columns. We may want to clean it first.

- create a separate sheet → select everything and transpose dataset so we should have **4** columns
- control + shift + right/down arrow to select everything then right click to transpose

![image](https://github.com/user-attachments/assets/d8a6ad8b-8313-4d28-8105-aad605d4f476)

![image](https://github.com/user-attachments/assets/e948bee1-193b-4579-a495-7f45517824a3)

- Further cleaning seeing theres a lot of **nulls** and some **blanks**. we can select all → data → filter
- control + h, replace null to blank since we want columns to be numeric

## Question 1:

What was the Yearly Debt Percentage Increase for each year compared to the previous year?

1. we can exclude year 2023 since theres no full months
2. we can only consider the last day of last month for each year, that is december 30/31
   
![image](https://github.com/user-attachments/assets/c572991b-7436-4edf-a9f8-9b74d5745ce8)

   
1. you can then calculate percent change by using the formula = (new year - prev year) / prev year *100
2. Now you can get other debt changes by dragging green dot

![image](https://github.com/user-attachments/assets/b3028950-3dcc-4249-8ca6-b763ed23a02a)


![image](https://github.com/user-attachments/assets/8535231a-8e99-4f04-b1e0-eec18aebb4da)


1. highlight all these, **insert** → **recommended charts** for visualization
2. you then need to sort years from smallest to largest for graph to show years chronologically

![image](https://github.com/user-attachments/assets/9485c704-ee6b-4520-bc62-1193e8b80ca9)


to type something like this, insert → textbox. Make sure for conclusion, **dig deeper** to something readers might not think about. Sometimes you have to do **further research**

### Question 2:

to answer this question, we need to aggregate the dataset by using **PivotTABLE.**

![image](https://github.com/user-attachments/assets/df531425-cc4a-4664-b1c9-b03e7cba19ff)


click on a cell and generate pivot table on existing worksheet if it small table.

make sure the table is accurate and the range. Dont select column A and B

Note: we just want the month to be aggregate, so we can remove others. You can right click → pivotTable option to get field list back

![image](https://github.com/user-attachments/assets/be0a1d10-e05a-4afa-9b6a-555b04bd72c0)

- click value field setting to change to average

![image](https://github.com/user-attachments/assets/d6d0a646-6a0a-4b72-946e-279b6b50dbea)


Now, we can create charts by looking into **pivotcharts → bar chart can be good for this**

![image](https://github.com/user-attachments/assets/cb7f58f3-f017-45ee-9235-a5c06a47978b)


![image](https://github.com/user-attachments/assets/306c6628-9bbb-4dd2-ae62-e28ab3b951db)

again, for conclusion, make sure to dig little bit deeper than the chart.

### Question 3:

What is the projected growth of the publicly held debt in the next few years?

1. Most accurate predictive model in forecasting for Excel. 
    1. **Note: Python has better forecasting**
2. create a pivotTable of the cleandata
3. aggregated based on years then select **max** debt held by public debt

![image](https://github.com/user-attachments/assets/30860515-a66b-451e-9d16-152f7cf721fc)

![image](https://github.com/user-attachments/assets/05639ea9-848a-419a-b61c-dfdf5c09772a)

exponential smoothing method might be the most accurate in excel. Select correct data and years to generate prediction.

Click on triangle button to convert to number

![image](https://github.com/user-attachments/assets/ca6dcb8a-7e98-4749-ab25-0a2c8b7c02ae)

![image](https://github.com/user-attachments/assets/a726634a-6faa-48ce-813b-fd803277eb51)

## Final Information

![image](https://github.com/user-attachments/assets/d14bc676-d28e-47b8-b45e-64035e49a8c0)

![image](https://github.com/user-attachments/assets/67e41563-4adb-4edc-8bf0-a23227722f6a)

![image](https://github.com/user-attachments/assets/ce3032a6-1696-4825-847c-b15c336fbd41)
