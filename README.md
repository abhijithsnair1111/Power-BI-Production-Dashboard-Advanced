# Manufacturinng Overview Dashboards Power BI (Advanced)
Welcome to the Manufacturing Overview Dashboard Project 🚀  
This project is focused on creating an advanced Power BI Dashboard consisting of multiple pages for a manufacturing company specialized in production and distribution of goods accross multiple industries.

The Project is intented as a study to understant the elements that goes into creating a complex BI dashboard. The data used in this project was generated to reflect real world manufcturing data as close as possible by including variability, meaning it includes random defects and delays accross production stages.

#### Final [Interactive Dashboard]() in Power BI Service

## 📌 Project Overview
Create an advanced Power BI Dashboard for a manufactring by tracking the production processes for a fiscal year. The source data consist of production details for both the goods produced and the equipments involved in the production. The dashboard should be able to capture all the relevant details regarding both production and equipments. A larger overview of the manufacturing process including inportant details regarding both products and equipments as the main page and dedicated pages for products and equipments for indepth analysis should be present.

The project should follow the standard four stage process of
- **Data Cleaning and Standardization**
- **Data Medelling**
- **DAX Calculations**
- **Data Visualization**

Being able to derive business insight and analytical descision for Stakeholders and Analyst is is the primary goal of creating such a dashboard therefore he end product should be a clean and modern looking dashboard that follows in all the UI/UX principles for user friendly interaction.

---

## 📊 Dashboards


---

## 💡Project Outline
The Project is focused on creating a simple and interactive dashboard for an manufacturing unit to track the production details for a fiscal year. The standard approach is to go through the four step process of Cleaning, Modelling, Calculating and Visualizing.

The data source for this project consist of three tables, one fact table detailing the production details called `fact_production` and two other dimension table each with details concering the products and equipments, `dim_products` and `dim_equipments` respectively. This tables form a **Star Schema** pattern with the centre fact table and the surrounding dimension tables. Additionaly two other tabes should be formed, one to calculate the neccessary measures and one as a dedicated date table. All the tables should be adiquete to provide the neccessary details for a clean and medern looking ashboard that is both easy to use and contains all the insights that might be useful to take business desisions

### Data Cleaning and Standardization ⚙️
The source data file consist of three main tables

Production Fact table - [`fact_production`](dataset/fact_production.csv)  
Products Dimension table - [`dim_products`](dataset/dim_products.csv)  
Equipments Dimension table - [`dim_equipments`](dataset/dim_equipments.csv)

Each table consists of multiple columns that are both dimensional values and measure values. Each columns should be analysed to ensure that the follow the standard data conventions

- Remove any null values in the primary key columns
- Remove all the leading and trailing spaces in the character columns
- Ensure the values in the date column are of date format
- Chack the range of date column to ensure only values from a specific year
- Check the sanity of categorical columns
- Check the numerical columns for any other values
- Assign the correct data type to each column

After the data cleaning process the end data is clean normalized and standardized to move on to the modellig stage

### Data Modelling 🔗
All the tables in the source dataset follows the standard convention of one fact table and multiple dimension tables, thus the right approach when it comes to modelling the relationship between the data is to establist a **Star Schema** pattern between the tables. The fact fact table would be placed on the cnetre and all the dimension tables surround them as to provide additional information for the central table. Each dimension table in the dataset consist of a Primary key, uniquely identifying each distinct element in the dimension table, these primary key appear multiple times inside the fact table to reference a element, in this case the a specific product or an equipment. Thus these keys are used to form a one to many realtion between the dimension and fact table.

[data_model](docs.data_model.png)

### DAX Calculations 📐
The existing tables can only provide limited details when it comes to creating KPIs and other relevent metrics. Using Data Analytics Expressions (DAX) two other tables are created to make the visualization process easy and straight forward

The Measures table include relevent calcualtion that has been derived from the existing measure values

- Aggregated Values
  - `total_produced` - Sum of all the units produced
  - `total_cost` - Sum of all the cost for the production of each unit
  - `total_defective` - Sum of all the units that are defective
  - `good_units` - Total defective units substracted from total produced units
  - `waste_cost` - Sum of all the cost by defective units
  - `unit_cost` - Waste cost substracted from the total cost
  - `total_planned_units` - Sum of all the planned units
  - `projected_cost` - Sum of all the cost for the production of each planned unit
  - `production_to_target` - Total produced substracted from total planned unit

- Percentage Values
  - `yield%` - The percantage of good units among the total produced
  - `efficiency%` - The percantge of planned duration compared to actual duration
  - `performance%` - The percantage of total production to  planned production
  - `oee` - Overall Equipment Effectiveness (Multiplying Yield, Efficiency and Performance)
  - `scrap_rate` - The percentage of defective units to total production
  - `production_value` - The percentage of increase or decrease in total production compared to total planned production

- Time Series Value
  - `total_actual_duration1` - Sum of the production duration for each unit\
  - `planned_duration` - Sum of the duration for each planned units
  - `down_time_variance` - Planned duration substracted from actual duration
 
- Formatted Value
  - `total_time` - Actual duration formatted in hours and minutes
  - `planned_time` - Planned duration formatted in hours and minutes


















