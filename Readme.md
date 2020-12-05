# Guns? Guns.

**Extract**: The data we extracted are Data.world CSV files documenting firearm theft statistics from January 6, 2016 to May 25th,2020. Conducted by the Bloomington, IN police department, this data is broken down by the following:
* property number 
* date of incident 
* model of gun 
* weapon description 
* case status
* case number,
* police agency involved
* place where the weapon was stolen . 


**Transform**: Taking massive amounts of gun data and taking out extraneous elements like incident numbers, police agency designations, weapon description, and case numbers.

### Jupyter
1. We imported CSV files to Jupyter Notebooks.
2. Through the following Python code, we combined the CSV and XLSX files into one large table in Jupyter. 
    
3. We created a new table variable by filtering the combined table created in step 2. We filtered out the following columns: 
    Incident numbers
    police agency
    weapon description
    case numbers


**Load**: Pushing cleaned data from Jupyter Notebooks to SQL Postgres and then onto a GitHub repository.

### SQL (pgAdmin4)
1. Before exporting our combined CSV/XLXS Jupyter table into a relational SQL database, we had to create a SQL table with the following fields:

    Date
    Brand
    Stolen
    Stolen From
    Status
2. Since our pgAdmin database has been created, we then created our engine and database connection using Jupyter. 
3. Using <engine.table_names()>, we made sure that our SQL database has the right table before we export our Jupyter information to pgAdmin.
4. Finally, we exported our Jupyter code to pgAdmin using a <.to_sql> line from sqlalchemy.  

    

        
  

Once you have identified your datasets, perform ETL on the data. Make sure to plan and document the following:
## Analysis

**The sources of data that you will extract from.** 
https://data.world/city-of-bloomington/ff8cb100-017d-44ef-a05a-37a19ec44611 csv files relating to firearm theft statistics. 


**The type of transformation needed for this data (cleaning, joining, filtering, aggregating, etc).** 
We are concatenating csv files in Jupyter notebooks, dropping columns we feel are unnecessary.

The type of final production database to load the data into (relational or non-relational).
We will be loading our concatenated and cleaned data from Jupyter Notebooks onto relational pgAdmin 4 SQL table. 

The final tables or collections that will be used in the production database.
<Jupyter file name> and <file.sql>

