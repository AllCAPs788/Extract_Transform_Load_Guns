# Guns? Guns.

## Extract: 
The data we extracted are Data.world CSV and XLXS files documenting firearm theft statistics from January 6, 2016 to May 25th,2020. Conducted by the Bloomington, IN police department, this data is broken down by the following:
* property number 
* date of incident 
* model of gun 
* weapon description 
* case status
* case number,
* police agency involved
* place where the weapon was stolen . 

Source URL: https://data.world/city-of-bloomington/ff8cb100-017d-44ef-a05a-37a19ec44611

## Transform
 Taking massive amounts of gun data and taking out extraneous elements like incident numbers, police agency designations, weapon description, and case numbers.

### Jupyter
1. We imported CSV files to Jupyter Notebooks.
2. We combined the CSV and XLSX files into one large table in Jupyter. 
    
3. We created a new table variable by filtering the combined table created in step 2. The following columns were filtered out: 
    * Incident numbers
    * police agency
    * weapon description
    * case numbers


## Load 
Pushing cleaned data from Jupyter Notebooks to SQL Postgres and then onto a GitHub repository.

### SQL (pgAdmin4)
1. Before exporting our combined CSV/XLXS Jupyter table into a relational SQL database, we had to create a SQL table with the following fields:

    * Date
    * Brand
    * Stolen
    * Stolen From
    * Status

2. Since our pgAdmin database has been created, we then created our engine and database connection using Jupyter. 
3. Using <engine.table_names()>, we made sure that our SQL database has the right table before we export our Jupyter information to pgAdmin.
4. Finally, we exported our Jupyter code to pgAdmin using a <.to_sql> line from sqlalchemy.  

    

        
  










