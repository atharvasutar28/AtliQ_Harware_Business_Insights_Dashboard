# AtliQ_Harware_Business_Insights_Dashboard
## Project Overview
AtliQ Hardware has grown rapidly in recent years, and they have decided to implement data analytics using PowerBi in their company for the first time to surpass their competitors in the market and to make data-driven decisions. This project is hoped to give answers to the questions of stakeholders in terms of all aspects like finance, sales, marketing, and supply chain.

I worked on this project by following the Codebasics PowerBi Course, Link to the course is [here](https://codebasics.io/bootcamps/data-analytics-bootcamp-with-practical-job-assistance)

[Live Report Link](https://app.powerbi.com/view?r=eyJrIjoiYTMwYmJhYjMtNmZjNi00NDkzLTgyYmEtNTU4ZTAwOGFhN2U5IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

Visit My Presentation Video on LinkedIn -> <a href="https://www.linkedin.com/feed/update/urn:li:activity:7243549037071609858/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="https://www.linkedin.com/feed/update/urn:li:activity:7243549037071609858/" height="30" width="40" /></a>

## Tech stacks
* SQL
* PowerBi Desktop
* Excel
* DAX language
* DAX studio (for optimizing the report)
## PowerBI techniques Learnt
* What are all the questions that should be asked before starting the project
* Creating calculated columns
* Creating measures using the DAX language
* Data modeling
* Using Bookmarks to switch between two visuals
* Page navigation with buttons
* Using the divide function to prevent zero division errors
* Creating date table using m language
* Dynamic titles based on the applied filters
* Using KPI indicators
* Conditional formatting of the values in visuals using icons or background color
* Data validation techniques
* PowerBi services
* Publishing reports to PowerBi services
* Setting up a personal gateway to set up the auto-refresh of data
* PowerBi App creation
* Collaboration, workspace, and access permissions in PowerBi services
* And more 😅
## Business related terms
* Gross price
* Pre-invoice deductions
* Post-Invoice deductions
* Net Invoice sale
* Gross Margin
* Net sales
* Net profit
* COGS - cost of goods sold
* YTD - Year to Date
* YTG - Year to Go
* Direct
* Retailer
* Distributors
* Consumer
## Company’s Background
AltiQ Hardware is a company that has grown vastly in recent years, and opened business all over the globe. It is a company that sells, computers and computer accessories through three mediums/channel
* Retailers
* Direct
* Distributors
Recently the company has faced an unforeseen loss by opening a store in America based on surveys, intuition, and some Excel analysis also the company’s competitors have a handful of analytics teams to perform analysis and make data-driven decisions. So, the AltiQ hardware has no other option other than building their analytics team for data-driven insights and decisions in the future to survive better in the industry.

Project kick-off session, where you should get clear of what and why this project is and all other questions you have with regards to the project

### Questions to ask before starting with the dashboard
* What is the objective of building this PowerBi dashboard?
* In what terms the success of this project will be measured?
* What will be the deadline for the project?
* Do the stakeholders expect a preview before the actual release?
* What are all the hopes stakeholders have out of this project?
* What are all the fears the stakeholders have in terms of building this dashboard?
* Who will be using this dashboard and for what purpose?
* What are all expectations the stakeholders have, by the completion of this project?
* What can go wrong while building this project?
* What are all the resources/ data needed to build this dashboard?
* Is there any input from stakeholders in terms of design and views of the dashboard?
After the project kick-off meetings, the data engineering team has given the data as per the request of the data analytics team, let’s explore them.

### Dataset Understanding
Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get a good understanding of what are data available.

Dimension table: It will have static data like details of customers and products

Fact table: It will have the data about the transactions

* gdb041:
  - dim_customer
    - 27 distinct markets (ex India, USA, Spain)
    - 75 distinct customers throughout the market
    - 2 types of platforms
      - Brick & Motors - Physical/offline store
      - E-commerce - Online Store (Amazon, Flipkart)
    - Three channels
      - Retailer
      - Direct
      - Distributors
  - dim_market
    - 27 distinct markets (ex India, USA, Spain)
    - 7 sub-zones
    - 4 regions
      - APAC
      - EU
      - nan
      - LATAM
  - dim_product
    - Divisions
      - P & A
        - Peripherals
        - Accessories
      - PC
        - Notebook
        - Desktop
      - N & S
        - Networking
        - Storage
    - There are 14 different categories, Like Internal HDD, keyboard
    - There are different variants available for the same product
  - fact_forecast_monthly
    - This table is used to forecast the customer’s needs in advance, which can help in
      - Higher customer satisfaction
      - Reduced cost in warehouses for storage purposes
    - The table is denormalized by the data engineering team, as it is a data warehouse that is aimed to be used for analytical work.
    - All the dates of the month will be replaced by the start date of the month
    - It will have all the column names and in the end, it will have the forecast quantity needed by the customer
  - fact_sales_monthly
    - This table is more or less same as the fact_forecase_monthly table, but the last column has the value of the sold quantity instead of the forecast value.
* gdb056
  - freight_cost
    - This table has details of travel cost and other cost for each market with fiscal year
  - gross_price
    - Has the details of gross prices with product code
  - manufacturing_cost
    - Has the details of manufacturing cost with product code with year
  - Pre_invoice_dedutions
    - Has the details of pre-invoice deductions percentage for each customer with year
  - Post_invoice_deductions
    - Post invoice deductions and other deduction details
## Importing Data into PowerBi
* As the database is MySQL in this project, we need to import the datasets from Mysql database to PowerBi by providing the Database access credential
## Data Model
* Data modeling plays a vital role and is considered as the basement of the report. All the visuals will be built upon the data model.
* Poor data modeling affects the overall performance of the report.
* Following Good practices of data modeling is a must. Refer to this page to get to know the good practices of Blog
* In this project, we have followed the Snowflake data modeling schema.
![Data Model](https://github.com/user-attachments/assets/616d21e3-a889-4d5b-b4d7-d9ab198052a0)


Dashboard designing
Based on the mock-ups received as required, the team will start designing the visuals and create measures as and when required.

Home view
In Home view, all the views button will be available. Users will land on a specific view page by clicking the button

* Home Page
* Info
* Finance View
* Sales View
* Marketing View
* Supply chain View
* Executive View
* Support

## Home Page
![Home Page](https://github.com/user-attachments/assets/8e671c90-c7bd-40ac-8756-e7347e7bde4a)

## Info Page
![Info Page](https://github.com/user-attachments/assets/9e7b76d7-2357-4159-b4dc-dc953589ca9e)

## Finance View
![Finance View](https://github.com/user-attachments/assets/a1637966-3671-40c2-9cbb-c7b7be1abcd1)

## Sales View
![Sales View](https://github.com/user-attachments/assets/5d3056bb-6b39-4f6b-bded-93476146343f)

## Marketing View
![Marketing View](https://github.com/user-attachments/assets/7df5b825-00e3-47a3-b956-581212233fed)

## Supply chain View
![Supply Chain View](https://github.com/user-attachments/assets/0516cbe2-765c-4f0c-913c-1c398c954486)

## Executive View
![Executive View](https://github.com/user-attachments/assets/b2c4fa0d-d8bc-456e-9c78-7d0f33f96d48)

## Support Page
![Support Page](https://github.com/user-attachments/assets/1aa0d5d8-575a-43b0-b321-9c0c7ac4c4c9)

## Project Outcome
1. Net Sales in the 2022 Fiscal Year are $ 3.74 Billion which is the most in all the years of AtliQ.
2. Dec 2021 recorded the highest Net Sales of the month in the history of AtliQ Hardware.
3. The Asia Pacific region contributed the most in the FY 2022.
4. Notebooks were the most sold segment for FY 2022.
5. Net Sales are almost 50% of the revenue and Gross Margin is almost 36% of the Net Sales in FY 2022.
6. The marketing department need to focus on Networking, Storage segments, and the Latin America region.
7. The Marketing Department needs to lower the operational expenses to increase the profit of the company.
8. Most of the customers are Out of Stock, Company needs to focus on manufacturing more products needed by the particular customers.
9. Finally, the stakeholders need to focus on increasing the market share and then increase their profits.
