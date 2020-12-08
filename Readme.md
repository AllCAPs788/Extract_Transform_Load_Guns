# Guns? Guns.
![Pistol](https://upload.wikimedia.org/wikipedia/commons/4/4f/SIG_Pro_by_Augustas_Didzgalvis.jpg)

## Extract: 
The data we extracted are Data.world [**CSV and XLXS files**](https://data.world/city-of-bloomington/ff8cb100-017d-44ef-a05a-37a19ec44611
) documenting firearm theft statistics from January 6, 2016 to May 25th,2020. Conducted by the Bloomington, IN police department; this data is broken down by the following:
* property number 
* date of incident 
* model of firearm
* weapon description 
* case status
* case number,
* police agency involved
* place where the weapon was stolen . 


## Transform
 In this section, we imported four years of gun data and removed extraneous elements like incident numbers, police agency designations, weapon description, and case numbers. Once we transormed our data, we converted the data to a SQL table.
 
 Here is our detailed transformation process. 

### Jupyter Notebooks
1. We imported CSV and XLXS files to Jupyter Notebooks file, [**guns_8.ipynb**](https://github.com/AllCAPs788/ETL_group_7/blob/master/guns_7.ipynb).
2. We combined the CSV and XLSX files into one large table in Jupyter. 
    
3. We created a new table variable by filtering the combined table created in step 2. The following columns were filtered out: 
    * Incident numbers
    * police agency
    * weapon description
    * case numbers


## Load 
Pushing cleaned data from Jupyter Notebooks to SQL Postgres and then onto a GitHub repository.

### SQL (pgAdmin4)
1. Before exporting our combined CSV/XLXS Jupyter table into a relational SQL database, we created a database called **guns_db** with a table named **Guns** with the following columns:

    * Date
    * Brand
    * Stolen From
    * Status

2. Since our pgAdmin database has been created, we then created our engine and database connection using Jupyter. 
3. Using `<engine.table_names()>`, we made sure that our SQL database has the right table columns before we exported our Jupyter information to **guns_db**.
4. Finally, we exported our Jupyter code to pgAdmin using a `<.to_sql>` line from sqlalchemy onto our SQL table, [**guns.sql**](https://github.com/AllCAPs788/ETL_group_7/blob/master/guns.sql).

## Final Analysis

From our **guns_db** database, we found that guns were primarily stolen from the residences of gun owners. Most of these firearms were not recovered or were listed as "No Record". 

All of the weapons in the dataset were hand guns, and the most popular brands were Glock, Taurus, and Smith and Wesson.



        
  










