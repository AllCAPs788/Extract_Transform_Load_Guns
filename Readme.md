# Guns? Guns.

**Extract**: Data.world data from January 6, 2016- May 25th,2020 conducted by the Bloomington, IN police department on stolen guns. This data is broken down by property number, date of incident, model of gun, weapon description, case status, case number, police agency involved, and place where the weapon was stolen . 
**Transform**: Taking massive amounts of gun data and taking out extraneous elements like incident numbers, police agency designations, weapon description, and case numbers.

### Jupyter
1. Import csvs to jupyter
2. Through the following Python code, we combined the CSV and XLSX files into one large table in Jupyter. 
    
3. Drop the following columns after importing:
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
2. 

    

        
  

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

