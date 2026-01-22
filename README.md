# Manufacturinng Overview Dashboards Power BI (Advanced)
Welcome to the Manufacturing Overview Dashboard Project 🚀  
This project is focused on creating an advanced Power BI Dashboard consisting of multiple pages for a manufacturing company specialized in production and distribution of goods accross multiple industries.

The Project is intented as a study to understant the elements that goes into creating a complex BI dashboard. The data used in this project was generated to reflect real world manufcturing data as close as possible by including variability, meaning it includes random defects and delays accross production stages.

#### Final [Interactive Dashboard]() in Power BI Service

## 📌 Project Overview
Create an advanced Power BI Dashboard for a manufactring by tracking the production processes for a fiscal year. The source data consist of production details for both the goods produced and the equipments involved in the production. The dashboard should be able to capture all the relevant details regarding both production and equipments. A larger overview of the manufacturing process including inportant details regarding both products and equipments as the main page and dedicated pages for products and equipments for indepth analysis should be present.

The project should follow the standard four stage process of
- **Data Cleaning and Standardization**
- **DAX Calculations**
- **Data Medelling**
- **Data Visualization**

Being able to derive business insight and analytical descision for Stakeholders and Analyst is is the primary goal of creating such a dashboard therefore he end product should be a clean and modern looking dashboard that follows in all the UI/UX principles for user friendly interaction.

---

## 📊 Dashboards


---

## 💡Project Outline
The Project is focused on creating a simple and interactive dashboard for an manufacturing unit to track the production details for a fiscal year. The standard approach is to go through the four step process of Cleaning, Calculating, Modelling and Visualizing.

The data source for this project consist of three tables, one fact table detailing the production details called `fact_production` and two other dimension table each with details concering the products and equipments, `dim_products` and `dim_equipments` respectively. This tables form a **Star Schema** pattern with the centre fact table and the surrounding dimension tables. Additionaly two other tabes should be formed, one to calculate the neccessary measures and one as a dedicated date table. All the tables should be adiquete to provide the neccessary details for a clean and medern looking ashboard that is both easy to use and contains all the insights that might be useful to take business desisions

### Data Cleaning and Standardization ⚙️
The source data file consist of three main tables

Production Fact table - [`fact_production`](dataset/fact_production.csv)
Products Dimension table - [`dim_products`](dataset/dim_products.csv)
Equipments Dimension table - [`dim_equipments`](dataset/dim_equipments.csv)

Each table consists of multiple columns that are both dimensional values and measure values. Each columns should be analysed to ensure that the follow the standard data conventions

- Remove any null values in the primary key columns
- Remove all the leading and trailing spaces in the character columns
- Ensure their are not null values in the date column
- Assign the correct data type to each column





















