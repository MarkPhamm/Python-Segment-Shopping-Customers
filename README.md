# Customer Segmentation Using Python


## Introduction
Seamlessly integrated Spotify API to extract and analyze music data. 🎶 Leveraging Python, Amazon Web Services (AWS), and Amazon Quicksight, by building an end-to-end data ETL pipeline to process, transform, and visualize Spotify's rich music data.
The primary objective was to extract valuable insights from Spotify's extensive music catalog while constructing a comprehensive data pipeline to automate the entire process.

## Technology Used

**Programming Language**
- **Python:** We will use Python to create Lambda functions for the ETL pipeline
- **SQL:** We will leverage SQL queries for analysis on Amazon Athena

**AWS cloud** 
- **Amazon S3 (Storage):** Amazon S3 is a highly scalable object storage service that enables you to store and retrieve data of any size from anywhere on the web. It is commonly used for storing and distributing large media files, data backups, and static website files. 

- **AWS Lambda (Compute):** AWS Lambda is a serverless computing service that allows you to run code without the need to manage servers. You can use Lambda to execute code in response to various events, such as changes in Amazon S3, DynamoDB, or other AWS services.

- **Amazon CloudWatch (Logs/Trigger):** Amazon CloudWatch is a monitoring service for AWS resources and the applications you run on them. It provides the capability to track metrics, collect and monitor log files, and set up alarms for your resources.

- **AWS Glue Crawler (Data Crawler):** AWS Glue Crawler is a fully managed service that automatically scans your data sources, identifies data, and creates an AWS Glue Data Catalog.

- **AWS Glue Data Catalog (Data Catalog):** AWS Glue Data Catalog is a fully managed metadata repository that simplifies data discovery and management. You can easily integrate the Glue Data Catalog with other AWS services, such as Athena.

- **Amazon Athena (Analytics Query):** Amazon Athena is an interactive query service that simplifies the analysis of data in Amazon S3 using standard SQL. You can use it to analyze data stored in your Glue Data Catalog or other S3 buckets.- 

**Visualization tool** 
- **Amazon QuiqckSight (Data Visualization):** Amazon Quicksight is a cloud-based business intelligence service launched by Amazon Web Services in 2018 that provides fast, easy-to-use data visualization and analytics for companies to gain insights from their data.


## Architecture:
![image](https://github.com/MarkPhamm/Spotify-BI-Engineering-Project/assets/99457952/72f136f2-4ebd-4892-9685-f1bf552e2cd5)


## Pipeline
### **a. Test Spotify API using Jupiter notebook**
  - Step 1: Using Jupyter Notebook, test data and read JSON: RapidAPI, format dataframe, and create planning structure.

### **b. Data Extraction via Python on AWS**
  - Step 2: Use Python to create an AWS Lambda function to fetch the latest data from Spotify
  - Step 3: Create a trigger and run a cronjob every day to receive messages triggered daily by CloudWatch
  - Step 3: Save data to S3 storage as raw data for later transformation
![image](https://github.com/MarkPhamm/Spotify-BI-Engineering-Project/assets/99457952/02b54637-0389-44c0-9f74-0dfb825bb401)



### **c. Data Transformation**
  - Step 4: Write a Lambda function that receives object triggers and converts data to structure format (CSV)
  - Step 5: Add a trigger to receive the event and store the object in S3
  - Step 5: Save the data as transformation data to S3 Buckets

![image](https://github.com/MarkPhamm/Spotify-BI-Engineering-Project/assets/99457952/f8fd6d4f-dd0d-4a11-80f3-82056295c808)


### **d. Data Loading**
- Step 8: Build a crawler to collect data for Athena
- Step 9: Define the schema with AWS Glue

![image](https://github.com/MarkPhamm/Spotify-BI-Engineering-Project/assets/99457952/c71eabaa-8cef-4c17-8435-190fe45a637c)

![image](https://github.com/MarkPhamm/Spotify-BI-Engineering-Project/assets/99457952/d2bdcea1-3f4d-45e6-8b32-566f982bf3a5)


### **e. Analyze, Create Dashboard and Reports**
- Step 10: Analysing data with Athena
- Step 11: Connect Amazon Quicksight to Athena
- Step 12: Create keys KPI on Amazon Quicksight, build graphs and charts to communicate key insights

## Conclusions and Key Learning

* Building the extraction, transformation, and loading modules required learning new skills like AWS Lambda, CloudWatch, S3, Glue, Athena, and Python. The project demonstrated how these services can be integrated to ingest, process, store, and analyze data efficiently at scale.

* Automating the pipeline with triggers and schedulers was an important learning. This ensures latest data is processed daily without any manual intervention.

* Transforming the raw JSON data into an optimized CSV structure required problem-solving skills to parse and clean the data into the target schema.

* Loading the processed data into S3 and Athena enabled running SQL queries on terabytes of data and generating insights rapidly. These are powerful big data capabilities unlocked by the pipeline.

* Overall, this project provided hands-on experience in architecting, developing, and deploying a robust data pipeline on AWS. The skills learned will be invaluable for tackling more complex data engineering challenges in the future.


