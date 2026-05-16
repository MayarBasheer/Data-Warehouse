# Movie Rental Data Warehouse

## Project Overview
This project implements a complete Data Warehouse solution for a movie rental business using the Sakila OLTP database. The project includes dimensional modeling, ETL design, analytical queries, and visualizations to support business intelligence and decision-making.

The operational Sakila database was transformed into a dimensional analytical model using fact tables and dimension tables organized in a Hybrid Star Schema.

---

## Technologies Used
- Python
- Pandas
- SQLAlchemy
- MySQL
- Jupyter Notebook
- Matplotlib
- MySQL Workbench

---

## Data Warehouse Design

### Fact Tables
- `fact_rental`
- `fact_payment`

### Dimension Tables
- `dim_customer`
- `dim_film`
- `dim_store`
- `dim_staff`
- `dim_date`
- `dim_location`

---

## ETL Process

### Extract
Data was extracted from the Sakila OLTP database tables including:
- rental
- payment
- customer
- film
- inventory
- store
- staff
- address
- city
- country
- category
- film_category
- language
- actor
- film_actor

### Transform
The transformation phase included:
- Joining related OLTP tables
- Removing duplicate records
- Handling missing values
- Creating surrogate keys
- Creating date keys
- Calculating rental duration
- Detecting late returns
- Standardizing text values

### Load
The transformed data was loaded into the `movie_rental_dw` data warehouse using Pandas and SQLAlchemy.

---

## Business Questions
The warehouse supports analytical questions such as:
- Which films are rented most frequently?
- Which films generate the highest revenue?
- Which customers generate the highest revenue?
- How does revenue change over time?
- Which stores perform best?
- Which films are returned late most often?

---

## Data Quality
The ETL process included several data quality checks:
- Duplicate detection
- Missing value handling
- Referential integrity validation
- Standardization of text and date values

Missing return dates were replaced using an unknown date key (`19000101`).

---

## Schema Type
The dimensional model mainly follows a Hybrid Star Schema design where fact tables reference descriptive dimensions using surrogate keys.

---

## Final Result
The final data warehouse supports:
- Rental trend analysis
- Revenue analysis
- Customer behavior analysis
- Store performance analysis
- Time-based reporting
- Geographic analysis

The project demonstrates how ETL and dimensional modeling can transform OLTP transactional data into a business intelligence solution suitable for reporting and decision-making.
