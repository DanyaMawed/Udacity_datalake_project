# Udacity_datalake_project

Divvy is a bike sharing program in Chicago, Illinois USA that allows riders to purchase a pass at a kiosk or use a mobile application to unlock a bike at stations around the city and use the bike for a specified amount of time. The bikes can be returned to the same station or to another station. The City of Chicago makes the anonymized bike trip data publicly available for projects like this where we can analyze the data.

Since the data from Divvy are anonymous, we have generated fake rider and account profiles along with fake payment data to go along with the data from Divvy. The dataset looks like this:

This image represents the data model for the dataset based on the Divvy Bikeshare data. The tables include: Rider, Account, Payment, Trip, and Station.
![image](https://github.com/DanyaMawed/Udacity_datalake_project/blob/0b579cfdb0d98e445481d6677793ab2da502af6c/Images/dend-project-erd.jpeg)

The goal of this project is to develop a data lake solution using Azure Databricks using a lake house architecture. You will:

- Design a star schema based on the business outcomes listed below;
- Import the data into Azure Databricks using Delta Lake to create a Bronze data store;
- Create a gold data store in Delta Lake tables;
- Transform the data into the star schema for a Gold data store;

The business outcomes you are designing for are as follows:

1- Analyze how much time is spent per ride
- Based on date and time factors such as day of week and time of day
- Based on which station is the starting and / or ending station
- Based on age of the rider at time of the ride
- Based on whether the rider is a member or a casual rider
  
2- Analyze how much money is spent  
- Per month, quarter, year
- Per member, based on the age of the rider at account start
 
3- Analyze how much money is spent per member
- Based on how many rides the rider averages per month
- Based on how many minutes the rider spends on a bike per month

  ## Step 1 - Star Schema
    ![image](https://github.com/DanyaMawed/Udacity_datalake_project/blob/0b579cfdb0d98e445481d6677793ab2da502af6c/star%20schema%20.png)

  ## Step 2 - Create Cluster and enable DPFS browse
    ![image](https://github.com/DanyaMawed/Udacity_datalake_project/blob/0b579cfdb0d98e445481d6677793ab2da502af6c/Images/creating%20cluster.png)
  
    ![image](https://github.com/DanyaMawed/Udacity_datalake_project/blob/0b579cfdb0d98e445481d6677793ab2da502af6c/Images/DBFS%20enable.png)
  
  ## Step 3 - Import csv files to Databricks DBFS
   ![image](https://github.com/DanyaMawed/Udacity_datalake_project/blob/0b579cfdb0d98e445481d6677793ab2da502af6c/Images/Upload%20data%20.png)
   ![image](https://github.com/DanyaMawed/Udacity_datalake_project/blob/0b579cfdb0d98e445481d6677793ab2da502af6c/Images/Data%20in%20DBFS.png)
  ## Step 4 - Import the data into Azure Databricks using Delta Lake to create a Bronze data store
   ![image](https://github.com/DanyaMawed/Udacity_datalake_project/blob/0b579cfdb0d98e445481d6677793ab2da502af6c/Images/ingest%20data%20from%20the%20DBFS%20into%20Delta%20tables.png)
  
  ## Step 5 - Create delta tables
   ![image](https://github.com/DanyaMawed/Udacity_datalake_project/blob/0b579cfdb0d98e445481d6677793ab2da502af6c/Images/loading%20data.png)
  
  ## Step 6 - Transform the data into the star schema for a Gold data store;
   ![image](https://github.com/DanyaMawed/Udacity_datalake_project/blob/0b579cfdb0d98e445481d6677793ab2da502af6c/Images/transform%20.png)


  
