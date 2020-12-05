# Guns? Guns.

**E**: Data.world data from January 6, 2016- May 25th,2020 conducted by the Bloomington, IN police department on stolen guns. This data is broken down by property number, date of incident, model of gun, weapon description, case status, case number, police agency involved, and place where the weapon was stolen . 
**T**: Taking massive amounts of gun data and taking out extraneous elements like incident numbers, police agency designations, weapon description, and case numbers.



**L**: Pushing cleaned data from Jupyter Notebooks to SQL Postgres and then onto a GitHub repository.


## Schedule: 
Saturday: Creating both jupyter and postgres tables
    Gabe: Jupyter work with csv
    Clark and Essi: setting up SQL table for transfer from Jupyter

## Saturday goals:
    Import csvs to jupyter
        Drop the following fields after importing:
            Incident numbers
            police agency
            weapon description
            case numbers

    
    Create SQL relational database from the same fields being used in jupyter

Monday: final SQL additions and analysis wrap-up

Go team. yaaaay.

Once you have identified your datasets, perform ETL on the data. Make sure to plan and document the following:


The sources of data that you will extract from. https://data.world/city-of-bloomington/ff8cb100-017d-44ef-a05a-37a19ec44611 csv files relating to firearm theft statistics. 


The type of transformation needed for this data (cleaning, joining, filtering, aggregating, etc). 
We are concatenating csv files in Jupyter notebooks, dropping columns we feel are unnecessary.

The type of final production database to load the data into (relational or non-relational).
We will be loading our concatenated and cleaned data from Jupyter Notebooks onto relational SQP Postgres table. 

The final tables or collections that will be used in the production database.


You will be required to submit a final technical report with the above information and steps required to reproduce your ETL process.