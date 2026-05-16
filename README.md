# Informatica-Project

This Informatica project demonstrates the implementation of multiple ETL (Extract, Transform, Load) concepts using different transformations and Oracle database connections. The main objective of the project is to extract data from source systems, apply business logic and validations, and load the processed data into target tables for analysis and reporting.

Project Components Used
🔹 Source and Target Connections
Oracle Source Connection
Used to connect Informatica with the source Oracle database.
Data is extracted from source tables for processing.
Oracle Stage Connection
Used as the staging or target database connection.
Processed and validated records are loaded into stage/target tables.
Transformations Implemented
1️⃣ Filter Transformation (FILTER_PROJECT)
Purpose
Used to filter records based on specific conditions.
What You Have Done
Extracted records from the source table.
Applied filtering logic to allow only required records.
Removed unwanted or invalid data before loading.
Example
Filtering only:
Active customers
Valid records
High-value transactions
Benefit
Reduces unnecessary data processing.
Improves ETL performance.
2️⃣ Router Transformation (router VALID CHECKING)
Purpose
Used to split records into multiple groups based on conditions.
What You Have Done
Implemented validation checking logic.
Routed:
Valid records → Valid output group
Invalid records → Reject/Error group
Example
If salary > 0 → Valid Group
If salary is NULL or negative → Invalid Group
Benefit
Helps manage multiple business conditions in one transformation.
Makes error handling easier.
3️⃣ Aggregator Transformation (AGG_PROJECT)
Purpose
Used to perform calculations and summary operations.
What You Have Done
Calculated aggregate values such as:
SUM
COUNT
AVG
MAX
MIN
Example
Total sales by department
Average salary by employee role
Benefit
Useful for reporting and analytics.
Reduces manual calculations in databases.
4️⃣ Rank Transformation (rank)
Purpose
Used to rank records based on specific columns.
What You Have Done
Sorted and ranked records.
Selected:
Top performers
Highest salaries
Best-selling products
Example
Top 5 employees by salary
Highest power consumption devices
Benefit
Helps identify top or bottom records efficiently.
5️⃣ Sequence Generator (Sequence)
Purpose
Generates unique sequential values.
What You Have Done
Created unique IDs for target records.
Used sequence numbers while loading data.
Example
Employee_ID
Transaction_ID
Customer_ID
Benefit
Ensures uniqueness in target tables.
Useful for surrogate key generation.
