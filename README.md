**ETL Mini-Project**
**Project Overview:** This ETL (Extract, Transform, Load) mini-project focused on building a data pipeline using Python, Pandas, and PostgreSQL. The goal was to process and transform data from Excel files into structured formats, store them as CSV files, and load them into a PostgreSQL database. The final deliverables included a complete ETL pipeline, database schema, CSV exports, and an interactive ERD (Entity Relationship Diagram).

Key Deliverables:
**1. Data Extraction and Transformation**
**Category DataFrame:**

Extracted unique categories from crowdfunding.xlsx.
Created a category_id column (e.g., cat1, cat2).
Exported the DataFrame to a category.csv file.
Subcategory DataFrame:

Extracted unique subcategories.
Created a subcategory_id column (e.g., subcat1, subcat2).
Exported the DataFrame to subcategory.csv.
Campaign DataFrame:

Extracted and transformed relevant columns from crowdfunding.xlsx.
Adjustments included:
Renaming columns for clarity (e.g., "blurb" → "description").
Converting goal and pledged to float.
Converting UTC timestamps in launched_at and deadline to human-readable datetime format.
Merged category_id and subcategory_id for relational consistency.
Exported the final DataFrame to campaign.csv.
Contacts DataFrame:

Extracted data from contacts.xlsx using Python dictionary methods or regular expressions.
Split the "name" column into first_name and last_name.
Cleaned and standardized email addresses.
Exported the transformed data to contacts.csv.
**2. Database Design and Implementation**

**ERD Creation:**

Designed an Entity Relationship Diagram (ERD) to represent relationships between the four main entities: category, subcategory, campaign, and contacts.

**Database Schema:**

Created a PostgreSQL schema (crowdfunding_db_schema.sql) defining tables, primary keys, foreign keys, and constraints.

**Key relationships included:**
category_id and subcategory_id in the campaign table linking to the respective tables.
contact_id linking the campaign and contacts tables.

**Database Creation:**

Created a PostgreSQL database named crowdfunding_db.
Executed the schema to create the tables in the correct order to handle dependencies.

**Data Loading:**

Imported the CSV files into their respective database tables without errors.
Verified data integrity using SELECT * statements for each table.
**Requirements Fulfilled:**
**Category DataFrame:** Created and exported with sequential category_id values and category titles.
**Subcategory DataFrame:** Created and exported with sequential subcategory_id values and subcategory titles.
**Campaign DataFrame:** Includes all required columns with proper transformations, exported as campaign.csv.
**Contacts DataFrame:** Includes contact_id, first_name, last_name, and email columns, exported as contacts.csv.
**Database Setup:**
Schema with appropriate constraints and relationships.
All CSV files successfully imported into PostgreSQL tables.
**Outcome and Value:**
This project successfully delivered a fully operational ETL pipeline. The resulting database enables efficient storage, querying, and analysis of crowdfunding data. The structured process demonstrated key ETL concepts and ensured data consistency across all outputs. Additionally, the collaborative aspect enhanced teamwork and problem-solving skills, preparing participants for real-world data engineering challenges.
