

<h4 align='center'> Leveraging <a href='https://aws.amazon.com/' target='_blank'>AWS Cloud Services,</a> an ETL pipeline transforms YouTube video statistics data. Data is downloaded from <a href='https://kaggle.com/datasnaek/youtube-new'>Kaggle</a>, uploaded to an S3 bucket, and cataloged using AWS Glue for querying with Athena. AWS Lambda converts to Parquet format and stores it in a clean S3 bucket. AWS QuickSight then visualizes the materialised data, providing insights into YouTube video performance. </h4>

## Overview


This project utilizes AWS Cloud Services to build an efficient ETL pipeline for processing YouTube video statistics data. The data, available [here](https://kaggle.com/datasnaek/youtube-new), is downloaded from Kaggle and uploaded to an S3 bucket. AWS Glue catalogs the data, enabling seamless querying using Amazon Athena. The pipeline processes both JSON and CSV data, converting them into Parquet format. JSON data is transformed using AWS Lambda functions with AWS Data Wrangler layers, while CSV data is processed through visual ETL jobs in AWS Glue.

Data is first stored in a raw S3 bucket, then cleaned and organized in a cleansed bucket, and finally joined and stored in an analytics or materialized bucket. Automated ETL jobs run daily using AWS Glue workflows, ensuring up-to-date data processing. A simple QuickSight dashboard visualizes the cleansed data, providing valuable insights into YouTube video performance across different regions. This setup ensures a scalable and efficient data processing workflow, facilitating detailed analysis and reporting.



The repository directory structure is as follows:
```
├── assets/                        
│   └── (Contains images, architecture and quicksight dashboard)
│
├── data/                          
│   ├── rawdataset/                     
│   ├── cleanseddataset/                 
│   └── data_analytics/
│
├── scripts/                                      
│   ├── etl_pipeline_csv_to_parquet.py             
│   ├── lambda_function.py                        
│   └── etl_S3_test_event.py         
│
├── README.md                      

```



## Tools 

To build this project, the following tools were used:

- AWS S3
- AWS Glue
- AWS Lambda/Layers
- Amazon Athena
- AWS QuickSight
- AWS Data Wrangler
- AWS Cloudwatch
- AWS IAM
- Python
- Pandas
- Spark
- Git

## Architecture

Following is the architecture of the project.

<p align='center'>
  <img src='https://github.com/sindhubommali01/Youtube_Data_Pipeline_AWS/blob/main/assets/AWS_Python_ETL_Project_Architecture.png' height=385 width=650>
</p>  

## Dashboard

Access simplified dashboard from <a href='https://github.com/sindhubommali01/Youtube_Data_Pipeline_AWS/blob/main/assets/dashboard.pdf'>here</a>.


## Screenshots

Following are project execution screenshot from AWS portal.

<img src="https://github.com/sindhubommali01/Youtube_Data_Pipeline_AWS/blob/main/assets/S3_Buckets.png" width=900 height=400>
<br>

