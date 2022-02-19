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

## **Analyzing with Pandas**

**Once the data is loaded to Pandas in a csv file, more subsets and dataframes were created to filter results needed to perform the analysis.**

![(1)](https://user-images.githubusercontent.com/91576834/154756273-974ef91e-357b-4e6c-9437-4592a2f8c33b.png)

## **Results**

**I have created the below reviews summary for vine vs no vine reviews for Amazon Sports equipment.**

![Screen Shot 2022-02-18 at 3 26 00 PM](https://user-images.githubusercontent.com/91576834/154774206-c8417766-e9b9-48da-937e-15988266569c.png)
![Screen Shot 2022-02-18 at 3 27 38 PM](https://user-images.githubusercontent.com/91576834/154774498-4bb4d807-1b30-4fba-a65a-e809e36e68ef.png)

- **In total there were 61,948 reviews of sports equipment, with approximate 5% vine reviews and 95% non-vine reviews.**
- **139 of vine reviews are 5 star, while 32,665 of non-vine reviews are 5 star.**
- **42% of vine reviews are 5 star, as well as 53% of non-vine reviews are 5 star.**

## **Summary**

**Based on the data summary, there is sufficent evidence of positvity bias for reviews in the Vine program. The non-vine reviews are approximately 10% higher in 5 star ratings compared to vine reviews.**

## **Further Analysis**

**To provide a more in-depth analysis on customer votes and reviews. Adding "helpful_votes" as a factor in the contribution of sports equipment being purchased can help distinguish if 5-star ratings play a factor in purchases.**








