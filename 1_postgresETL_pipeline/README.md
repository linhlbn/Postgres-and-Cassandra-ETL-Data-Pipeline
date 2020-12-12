| Table of Content |
| --- |
| I/ Purpose of the project |
| II/ Context |
| III/ Star Schema Database |
| IV/ Directory structure |
| V/ How it works? |


# I/ Purpose of the project

The project is a series of practical concept from Udacity DEND with:
* Data modeling  
* Create a Postgres database with star schema  
* ETL Postgres pipeline with Python  


# II/ Context
Sparkify - A startup wants to analyze data collecting from user activity on their music streaming app. The data analyst and scientist obsessed with data, they really want to dig deeper to see the insight. Unfortunately, they would not be easily to handle the data which resides in a directory of JSON logs as well the JSON metadata. My mission is to design a database and ETL pipeline for my analytics team.  


# III/ Star Schema Database
The primary key of this method is that we devide dataset into fact table containing the metadata of complete information about each user activities (songplays) and 4 dimension tables having detailed information about single row from facts table (users, songs, artists, time). Many dimension tables are connected to one fact table.  


# IV/ Directory structure
0. create_tables.py - Script contains postgresql queries creating the db and tables.
1. data - Folder contains the log and song datasets.  
2. etl.ipynb - Create step by step the pipeline before putting code into production (etl. py).  
3. etl. py - script contains the complete ETL pipeline.  
4. readme. md - Documentation  
5. sql_queries.py - Script covers the staging step in ETL process by creating and inserting data to the database.  
6. test.ipynb - Check the script for creating tables and inserting data are working okay or not.  


# V/ How it works?
0/ Ensure all files are located in the same place.    
1/ Open terminal and run below command to make sure all the previous databases will be dropped as well as new database with new tables could be created:  
```
    python create_tables.py
```

2/ After a while for staging, the database has been ready for ETL pipeline, run this command to extract, load data from source to fact and dimension tables.  

```
    python etl.py
```
