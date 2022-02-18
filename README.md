# Amazon_Vine_Analysis
 **Performing ETL and data Analysis on Amazon Sport Product Reviews to determine bias of favorable vine reviews**
 
 ## Overview
 
 **The purpose of this projec is to uncover favorabilty of Vine program reviews by analyzing Amazon sport product reviews. In order to analyze and uncover any bias reviews a large amount of review data must be processed using Pyspark, AWS, Postgress and lastly analyze the date with Pandas.**
 
 ## Database Schema Postgres
 
 **In order to properly process and analyze review data, I have created a Postgress database schema within AWS to load the data into once it is transformed.**
 
![Screen Shot 2022-02-17 at 8 11 26 PM](https://user-images.githubusercontent.com/91576834/154617100-753ea518-70a2-45a7-979d-6d422ee057a1.png)

## ETL PySpark Process 

### **Step 1 process:**

**Pyspark is first used to extract ad read in review data from an Amazon S3 Data storage server.**

![Screen Shot 2022-02-17 at 8 35 31 PM](https://user-images.githubusercontent.com/91576834/154618350-a4b368be-eea6-4e0b-a3ab-86a28a52d48b.png)

### **Step 2 process:**

**Pyspark is than used to transform the data by creating Dataframes form subsets, which will match the tables within the Postgress database and schema constraints. Once the dataframes are created, they are then loaded from AWS storage server to Postgres database**

![Screen Shot 2022-02-17 at 8 31 48 PM](https://user-images.githubusercontent.com/91576834/154618802-6e8d4097-70e8-4c47-979c-f7135783d818.png)





