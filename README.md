# Content
[Problem Statement](#Problem-Statement)
[Question 1](#Question-1)

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

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/4dacb6d7-f4c0-4345-ade2-2e3363b22d9f/image.png)

1. you can then calculate percent change by using the formula = (new year - prev year) / prev year *100
2. Now you can get other debt changes by dragging green dot

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/024504ac-f363-492d-826f-2875a38c91a9/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/d9f51f26-1d4c-43a8-8cd8-398324f1f05f/image.png)

1. highlight all these, **insert** → **recommended charts** for visualization
2. you then need to sort years from smallest to largest for graph to show years chronologically

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/629148c1-cba5-4892-8e92-aae8558738ba/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/51487dec-287c-48c5-b7bc-89e4e4193d5a/image.png)

to type something like this, insert → textbox. Make sure for conclusion, **dig deeper** to something readers might not think about. Sometimes you have to do **further research**

### Question 2:

to answer this question, we need to aggregate the dataset by using **PivotTABLE.**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/39fa4f78-a8ab-4eff-a1be-69ae2515b3e5/image.png)

click on a cell and generate pivot table on existing worksheet if it small table.

make sure the table is accurate and the range. Dont select column A and B

Note: we just want the month to be aggregate, so we can remove others. You can right click → pivotTable option to get field list back

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/1cef4fd5-cece-4d84-8c48-b5f3f00a2c20/image.png)

- click value field setting to change to average

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/b057300c-8a6d-41b6-a6c7-ba891ec1d865/image.png)

Now, we can create charts by looking into **pivotcharts → bar chart can be good for this**

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/b738ad29-4071-40e9-99d1-f3f06f4b366e/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/efc6f37d-0656-4ae4-b42c-baae5ffce358/image.png)

again, for conclusion, make sure to dig little bit deeper than the chart.

### Question 3:

What is the projected growth of the publicly held debt in the next few years?

1. Most accurate predictive model in forecasting for Excel. 
    1. **Note: Python has better forecasting**
2. create a pivotTable of the cleandata
3. aggregated based on years then select **max** debt held by public debt

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/e94ddb2e-556b-4543-aca3-5a96fbb25afb/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/44726823-195e-4bb1-b443-47c366998844/image.png)

exponential smoothing method might be the most accurate in excel. Select correct data and years to generate prediction.

Click on triangle button to convert to number

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/ada312c1-00c4-4c91-89c9-a1f295d7dea1/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/41c3072e-d0d9-454a-b267-23d2cbc101d2/image.png)

## Final Information

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/37eac9fd-fdee-4075-9aee-4f40a44b0688/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/c9ee00f9-9360-41a5-b6da-0cf5ee6988f0/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/0f68b445-c614-4869-9b6e-26712255f069/133316dd-a6ef-4e0e-9e51-63e3c312a6e1/image.png)
