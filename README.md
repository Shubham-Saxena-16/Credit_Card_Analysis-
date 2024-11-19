
# **Comprehensive Credit Card Weekly Dashboard**

## Project Overview:
The primary objective of this project is to develop a powerful and interactive **Credit Card Weekly Dashboard** that provides real-time insights into essential performance metrics and trends. This dashboard is designed to empower stakeholders to monitor credit card operations, enhance business performance, identify growth opportunities, and mitigate risks through data-driven decisions.
## Key Objectives 

1. **KPI Measurement & Monitoring**
The dashboard will track and analyze critical credit card performance indicators, including:

-   Revenue Generated
-   Transaction Volume
-   Total Interest Earned
-   Delinquency Rate
-   Customer Acquisition Cost (CAC)
-   Customer Satisfaction Score (CSAT)

These KPIs enable businesses to gauge overall performance, identify strengths and weaknesses, and make informed decisions to enhance profitability and operational efficiency.

2. **Revenue Analysis by Time Period**
This feature provides an in-depth analysis of credit card transaction revenue over multiple timeframes, segmented by:

-   Quarters
-   Weeks
-   Months
The goal is to uncover revenue trends, seasonal impacts, and fluctuations in customer spending, offering valuable insights into periods of high or low transaction activity.

3. **Customer Spending & Card Category Insights**
-   The dashboard analyzes customer spending behavior across various card categories (e.g., Gold, Platinum) and expenditure types (e.g., Bills, Entertainment, Travel). By examining this data, businesses can better understand customer demographics, preferences, and spending patterns, ultimately refining their marketing and customer engagement strategies.

4. **Customer Segmentation Analysis**
This feature enables revenue analysis based on different customer demographics and metrics, such as:

-   Educational Level
- Job Type
-   Income Group
The aim is to explore how customer segments impact revenue generation and identify patterns to target specific customer groups more effectively.

5. **Week-on-Week Revenue Comparison**
-   The dashboard facilitates week-on-week revenue analysis, enabling businesses to detect trends, anomalies, and deviations from expected patterns. By closely monitoring revenue shifts, stakeholders can uncover promotional effects, seasonal trends, and market dynamics, driving timely interventions to seize revenue opportunities or address potential risks proactively.

By combining detailed transaction data with customer information, this dashboard serves as a powerful tool for businesses, enhancing their ability to track key metrics, optimize performance, and drive strategic growth.
## Acknowledgements

I would like to express my gratitude to all the platforms and tools that contributed to the successful completion of this project. The data used for the credit card dashboard analysis was **sourced from Kaggle**, providing invaluable insights into real-world credit card operations.

I would also like to acknowledge the tools used in developing this project:

- **Power BI:** For its robust data visualization and analysis capabilities, enabling the creation of an interactive and insightful dashboard.
- **Figma:** For designing the layout and user interface, ensuring a clean and intuitive user experience.
- **Coolors.co:** For assisting in generating the perfect color palette that enhanced the visual appeal of the dashboard.
- **Flaticon:** For providing the icons used in the project, which added a layer of clarity and professionalism to the design.

Each of these resources was instrumental in bringing this project to life, and I am deeply appreciative of their contributions, which made the project both functional and visually compelling.

## Software & tools
- Power BI
- SQL Server
- Figma
- Coolors.co
- Flaticon
## Data Source & Understanding

The dataset provides detailed information on **52 week credit card transactions** along with associated **customer details** for a comprehensive **analysis of spending behavior and transaction patterns** over a specified period. The data is structured to enable in-depth insights into credit card usage, spending trends, and customer profiles.

    Source: Kaggle
    Datasets: 2
    File Type: CSV
    Total Records: 10,293
    Total Columns: 33
    Data Span: January 2023 - December 2023
**Dataset Description**

-   **Transaction Details:** The dataset includes records of credit card transactions, providing information such as transaction amount, merchant category, transaction date, and payment method.

-   **Customer Information:** It contains demographic details of customers, allowing for segmentation and analysis of different customer profiles, which can include factors like age, income level, and geographical location.

-   **Spending Behavior Analysis:** The data is structured to facilitate various analyses, such as:

    -   **Spending Trends:** Identifying peak spending periods, average transaction values, and categories with the highest expenditure.
    -   **Customer Profiles:** Analyzing customer demographics to understand different spending patterns and preferences among various segments.
    -   **Transaction Patterns:** Examining the frequency and timing of transactions to identify behavioral trends over time.

**Key Data Attributes**
-   **Transaction Date:** The date when each transaction occurred.
-   **Transaction Amount:** The monetary value associated with each transaction.
-   **Merchant Category:** The category or type of merchant where the transaction took place (e.g., groceries, entertainment).
-   **Customer ID:** A unique identifier for each customer.
-   **Demographic Information:** Data related to customer age, income, and location.
**Objectives for Analysis**
-   **Understanding Spending Behavior:** Gain insights into how customers utilize their credit cards over time, identifying patterns and trends that can inform marketing strategies.
-   **Segmenting Customers:** Use demographic data to segment customers and tailor financial products or promotions based on spending habits.
-   **Monitoring Transaction Trends:** Analyze transaction patterns to detect anomalies or shifts in consumer behavior, which can be valuable for fraud detection and risk assessment.

## Data Cleaning & Preprocessing

### Data Cleaning Steps
-   Data cleaning is a crucial step in preparing the dataset for analysis. The following steps outline the key cleaning operations performed on the credit card dataset:

    **1. Checking Data Types**
    -   **Data Type Validation:** Ensure that all columns contain the correct data types. For instance, numeric values should not be present in categorical fields such as "Gender."
    **2. Handling Missing Values**
    -   **Identification of Missing Data:** Review the dataset for any missing or null values in critical fields (e.g., Transaction Amount, Customer ID).
    -   **Imputation or Removal:** Decide on strategies to handle missing values, which may include:
        -   Imputation with mean, median, or mode for numeric fields.
        -   Removal of rows with missing essential information.
3. **Outlier Detection**
    - **Statistical Analysis:** Use statistical methods (e.g., Z-score or IQR) to identify outliers in numeric fields such as Transaction Amount.
    - **Treatment of Outliers:** Determine whether to remove, cap, or adjust outlier values based on the context and business needs.
4. **Standardization of Categorical Variables**

    - **Normalization:** Ensure that categorical fields (e.g., Merchant Category, Gender) have consistent formatting (e.g., lowercase, no leading/trailing spaces).
    -   **Categorical Value Checks:** Verify that categorical variables do not contain unexpected or erroneous entries.
5. **Data Type Conversion**
    -   **Date Format Standardization:** Ensure all date fields are in a standard format (e.g., YYYY-MM-DD).
    -   **Numeric Type Checks:** Convert relevant fields to numeric types for analysis (e.g., Transaction Amount).
6. **Creating New Variables for Analysis**
-   **Bucketing Age and Income:** Create new columns to categorize customers into age and income groups using logical conditions, as explained in the provided methodology:
    
        Age groups could include: 20-30, 30-40, 40-50, 50-60, and 60+.

-   **Income groups might consist of:** Low Income , Medium Income and High Income. 
    
        Low Income (less than 35,000)
        Medium Income (35,000-70,000)
        and High Income (above 70,000).
7. **Validation Checks**
-   **Referential Integrity:** Ensure that all customer IDs in the transaction dataset correspond to valid customer records in the customer details dataset.
-   **Logical Checks:** Validate that the relationships between various fields make logical sense (e.g., transaction dates should not precede customer registration dates).

### SQL Queries for Data Creation (Importing Data)
- *Listing All Existing Databases*

            SELECT name,database_id,create_date,state_desc
            FROM sys.databases;
- *Creating a New Database*

        CREATE DATABASE ccdb;
- *Checking the Current Database Context*

        SELECT DB_NAME() AS CurrentDatabase;

-   *Switching to the Newly Created Database*

        USE ccdb;


-   *Verifying the Database Switch*

        SELECT DB_NAME() AS CurrentDatabase;


**Closing and Refreshing the Data** - *No specific command is listed here, but this step is a general reminder to ensure the session is properly closed and the SQL Server Management Studio (SSMS) is refreshed to reflect the new database changes.*

-   *Retrieving Data from Tables*

        SELECT * FROM dbo.credit_card;
        SELECT * FROM customer;

 **Additional Considerations**

    Permissions: Ensure you have proper permissions to create databases and access tables.
    Database Existence: Double-check whether the ccdb database already exists to avoid conflicts.
    SQL Context: Make sure you are working in the correct context of your SQL Server instance.



### SQL Queries for Data Cleaning

- SQL queries used to clean or preprocess the data
    - **Removing Duplicates**

                DELETE FROM credit_card_transactions 
                WHERE TransactionID IN ( 
                SELECT TransactionID
                FROM (
                    SELECT TransactionID, ROW_NUMBER() OVER (PARTITION BY TransactionDetails ORDER BY TransactionID) AS row_num
                    FROM credit_card_transactions
                ) t
                WHERE row_num > 1
                );
    
    - **Handling Missing Data** 

            UPDATE customer
            SET income = 0
            WHERE income IS NULL;

### Data Transformation & Calculations

-   **Calculating Total Revenue:**

        SELECT 
            SUM(TransactionAmount + InterestEarned + AnnualFees) AS TotalRevenue
        FROM 
            dbo.credit_card_transactions;

-   **Creating Aggregated Tables:**

        SELECT 
            CustomerID, AgeGroup, SUM(TransactionAmount) AS TotalSpend
        INTO 
            dbo.CustomerSpendSummary
        FROM 
            dbo.credit_card_transactions
        GROUP BY 
            CustomerID, AgeGroup;

### DAX Queries for Advanced Calculations

DAX (Data Analysis Expressions) queries used in Power BI for calculating key metrics. You can list them here:

   1)  Total Revenue (DAX):
    Total Revenue = SUM(Transaction[TransactionAmount]) + SUM(Transaction[InterestEarned]) + SUM(Transaction[AnnualFees])


2)  Week-on-Week Change in Revenue:

        WoW Revenue Change = 
        DIVIDE (
            CALCULATE(SUM(Transaction[Revenue]), Transaction[WeekNum] = WeekNum_Current),
            CALCULATE(SUM(Transaction[Revenue]), Transaction[WeekNum] = WeekNum_Previous)
        )

  3) Customer Acquisition Cost (CAC):
    CAC = DIVIDE(Total_Acquisition_Costs, COUNT(Customer[CustomerID]))
## Features

Here are some key features of the project:

-   **KPI Monitoring:** Tracks key metrics like total revenue, transaction volume, interest earned, and delinquency rates.

-   **Revenue Analysis by Time Period:** Analyzes revenue by quarters, weeks, and months to uncover patterns.

-   **Customer Segmentation:** Categorizes customers by age, income, education, and credit card category for targeted analysis.

-   **Week-on-Week Revenue Comparison:** Identifies significant revenue trends or anomalies on a weekly basis.

-   **Demographic Impact Analysis:** Segments revenue by customer demographics such as gender, educational level, and job type.

These features collectively provide detailed insights into business performance and customer behavior, enabling more informed decision-making and targeted strategies.
## Building Dashboards


## Insights

**Week-on-Week Insights (Week 53)**

-   **Revenue Growth:** Increased by 28.8% compared to the previous week.
-   **Customer Growth:** Active customers grew by 12.8%.
-   **Transaction Count:** Rose by 3.39%.
-   **Transaction Amount:** Increased by 35%.

**Year-to-Date (YTD) Overview**
-   **Total Revenue:** $57 million.
-   **Interest Earned:** $8 million.
-   **Cost-to-Revenue Ratio:** 1.74%.
-   **Activation Rate:** 57.5%.
-   **Delinquency Rate:** 6.06%.
-   **Average Utilization Ratio:** 13.47%.
-   **Customer Satisfaction Score:** 3.19/5.
**Customer Spending & Demographics**
-   **Age Group Contribution:** Customers aged 40-50 contribute 43.7% of total revenue ($25M).
-   **Popular Credit Cards:** Blue and Silver cards account for 93% of transactions.
-   **Top Spending Categories:** Bills (24.7%), Entertainment (17.3%), and Fuel (16.9%).

For more detailed insights, you can download the full report **available in my GitHub repository.**
## Customer Spending and Demographics Analysis

-   **Revenue by Gender:**

    -   **Male  :** 54.4% ($31M).
    -   **Female:** 45.6% ($26M).
-   **Top States:**
    -    Texas
    -    New York
    -   California 
    account for 68% of the total transaction amount.

-   **Job Type:** Businessmen contribute 31.3% of revenue.

-   **Income Level:** High-income customers contribute nearly 49% of the total revenue.

-   **Marital Status:** Married customers account for 50.6% of the revenue.
## Project Presentation
## Appendix
1. **Data Source**
- Kaggle provided the dataset, which includes credit card transactions, customer details, and spending patterns over the period from **January 2023 to December 2023.**

2. **Tools Used**
- **Power BI:** Utilized for data visualization and dashboard creation. Power BI enabled interactive data exploration, allowing for the dynamic presentation of KPIs and trends.
- **SQL Server:** Used for data storage, querying, and preprocessing. SQL Server provided a reliable platform to manage the dataset and optimize data for analysis.
- **Figma:** Used for designing the layout and interface of the dashboard, ensuring a user-friendly design with a clear, intuitive structure.
- **Coolors.co:** Assisted in generating color palettes that aligned with the overall design and branding, enhancing the dashboard’s visual appeal.
- **Flaticon:** Provided the icons used throughout the dashboard to visually represent different metrics and categories, improving the overall user experience.

3. **Key Performance Indicators (KPIs)**

The dashboard was built to track and visualize the following KPIs:

-   **Revenue Generated:** The total revenue from credit card transactions, analyzed by various time periods (quarter, week, month).
-   **Transaction Volume:** The number of credit card transactions over time.
-   **Total Interest Earned:** The amount of interest earned from credit card holders.
-   **Delinquency Rate:** The percentage of cardholders who have overdue payments.
-   **Customer Acquisition Cost (CAC):** The cost associated with acquiring a new credit card customer.
-   **Customer Satisfaction Score (CSAT):** A measure of customer satisfaction, based on collected feedback or transaction data patterns.

4. **Analysis Metrics**
-   **Revenue Analysis by Quarter, Week, and Month:** The dashboard segmented revenue data by time period to help identify trends and seasonality in credit card usage.
-   **Customer Segmentation:** Customer behaviors and spending patterns were analyzed across various card categories (e.g., gold, platinum) and demographics (e.g., education level, income group).
-   **Week-on-Week Comparison:** This feature helped stakeholders track revenue fluctuations and anomalies on a weekly basis, highlighting emerging trends or potential areas of concern.

5. **Design and User Experience**

-   The dashboard layout was carefully designed to ensure an intuitive and user-friendly experience, allowing users to easily navigate through the metrics and derive insights from the data. Figma was instrumental in the design phase, providing a seamless process for crafting an effective visual structure.

6. **Visual Enhancements**
-   The use of icons from Flaticon helped communicate information clearly, while the color scheme generated by Coolors.co ensured the dashboard had a cohesive and visually appealing look, making the data easy to interpret.


## Authors

- [Shubham Saxena](https://github.com/Shubham-Saxena-16) 
A performance analyst with expertise in data analysis.

## Badges

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)
![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)

## Deployment

To deploy this project run,follow these steps:

1. **Clone the Repository:**

```bash
  git clone https://github.com/Shubham-Saxena-16/Credit_Card_Analysis
```
2. **Navigate to the Project Directory:**
```bash
  cd Credit_Card_Analysis
```

3. **Set Up the SQL Server Database:**
-   Ensure that you have SQL Server installed and running.
-   Create a new database  (ccdb) for the project.
-   Import the provided CSV data into the SQL Server database.

4. **Connect Power BI to SQL Server:**
-   Open Power BI Desktop.
-   Go to Home > Get Data > SQL Server.
-   Enter the SQL Server details (server name and database name) to connect.
-   Load the necessary tables for analysis.

5. **Build Your Dashboards:**
-   Utilize the imported data in Power BI to create the required dashboards.
-   Configure any necessary measures, calculations, and visuals as per the project requirements.

6. **Publish Your Power BI Reports:**
-   Once your dashboards are ready, you can publish them to the Power BI service for sharing and collaboration.

7. **Access the Application:**
-   Once published, access your Power BI dashboards via the Power BI service on your web browser.
## FAQ

#### Question 1 : What is this project about?

Answer 1 : The project aims to develop a comprehensive credit card weekly dashboard that provides real-time insights into key performance metrics and trends related to credit card operations, enabling stakeholders to effectively monitor and analyze credit card transactions and customer behavior.

#### Question 2 : What tools or libraries are used for analysis?

Answer 2: The project utilizes SQL Server for data storage and management, Power BI for data visualization and dashboard creation, Figma for design, Coolors.co for color palette generation, and Flaticon for icons to enhance the user interface.

#### Question 3 :What insights can be gained from the analysis?

Answer 3: The dashboard provides insights into various key performance indicators (KPIs) such as total revenue, transaction volume, customer acquisition costs, delinquency rates, and customer satisfaction scores, as well as trends in customer spending habits and preferences across different demographics and card categories.

#### Question 4 :Is the dataset provided with the project?

Answer 4: Yes, the project includes a dataset sourced from Kaggle, containing detailed information on credit card transactions and customer profiles. Users can also use their own datasets by following the provided data import instructions.

#### Question 5 :How can I contribute to the project?

Answer 5: Contributions are welcome! You can help by adding new features, improving existing functionalities, fixing bugs, or suggesting enhancements. Simply fork the repository, implement your changes, and submit a pull request for review.


## 🚀 About Me
I'm Shubham Saxena, a performance analyst specializing in insight generation, storytelling and data analysis. With a background in computer science, I excel in optimizing systems and processes to enhance performance and efficiency. I'm passionate about leveraging data-driven insights to drive strategic decisions and improve outcomes. Let's connect on LinkedIn to explore potential collaborations!

