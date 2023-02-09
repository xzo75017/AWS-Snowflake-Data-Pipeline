# Business Overview

Snowflake's Data Cloud is based on a cutting-edge data platform delivered as a service (SaaS). Snowflake provides data storage, processing, and analytic solutions that are quicker, easier to use, and more versatile than traditional options.
Snowflake isn't based on any current database technology or large data software platforms like Hadoop. Snowflake, on the other hand, combines a brand-new SQL query engine with cutting-edge cloud architecture. Snowflake gives users all the features and capabilities of an enterprise analytic database, plus a lot more.
There is no hardware to choose, install, configure, or manage (virtual or actual).  
There isn't much to install, set up, or maintain in terms of software.   
Snowflake oversees ongoing maintenance, administration, updates, and tweaking.  
Snowflake is entirely based on cloud infrastructure. Except for optional command-line clients, drivers, and connectors, all components of Snowflake's service operate on public cloud infrastructures.  
Snowflake's computing demands are met by virtual compute instances, and data is stored permanently via a storage service. Snowflake isn't compatible with private cloud environments (on-premises or hosted).  
The architecture of Snowflake is a mix of classic shared-disk and shared-nothing database designs. Snowflake employs a central data repository for persistent data, like shared-disk architectures, available from all compute nodes in the platform. Snowflake executes queries utilizing MPP (massively parallel processing) compute clusters, wherein each node in the cluster stores a part of the whole data set locally, like shared-nothing architectures. This method combines the simplicity of a shared-disk design with the speed and scale-out advantages of a shared-nothing architecture.  
In this project, we will create a data pipeline starting from the EC2 logs to storage in Snowflake and S3 post-transformation and processing through Airflow DAGs. This is the second project in the Snowflake project series, the first project being an introduction to different Snowflake components and their uses.  

 
## Dataset used  

Two CSV files are used for project implementation with various fields- 

customers.csv  

orders.csv  

 

## Data Pipeline  

A data pipeline is a technique for transferring data from one system to another. The data may or may not be updated, and it may be handled in real-time (or streaming) rather than in batches. The data pipeline encompasses everything from harvesting or acquiring data using various methods to storing raw data, cleaning, validating, and transforming data into a query-worthy format, displaying KPIs, and managing the above process. In this project, two streams of data are added to Snowflake and S3 processed stage through Airflow DAG processing and transformation- customers data and orders data.  

 

Tech Stack:  

- Languages: SQL, Python3  

- Services: Amazon S3, Snowflake, Amazon MWAA, Amazon Kinesis Firehose, AWS EC2  

 

## Amazon MWAA    

Amazon Managed Workflows for Apache Airflow (MWAA) is a managed orchestration solution for Apache Airflow1 that makes setting up and operating end-to-end data pipelines in the cloud at a scale much easier. Apache Airflow is an open-source application for authoring, scheduling, and monitoring process and task sequences known as "workflows" in a programmatically controlled manner. Using Managed Workflows, you can develop workflows with Airflow and Python without having to worry about scalability, availability, or security of the underlying infrastructure.  

 

## AWS EC2

A virtual server on Amazon's Elastic Compute Cloud (EC2) for executing applications on the Amazon Web Services (AWS) architecture is known as an Amazon EC2 instance. The Amazon Elastic Compute Cloud (EC2) service allows corporate customers to run application applications in a computer environment. Using Amazon EC2 eliminates the need to invest in hardware up front, allowing users to create and deploy apps quickly. Amazon EC2 allows users to launch as many or as few virtual servers as they want, set security and networking, and manage storage.  

 

## Amazon S3   

Amazon S3 is an object storage service that provides manufacturing scalability, data availability, security, and performance. Users may save and retrieve any quantity of data using Amazon S3 at any time and from any location.  

 

## Amazon Kinesis Firehose  

Amazon Kinesis Data Firehose is a fully managed service that delivers real-time streaming data to Amazon S3, Amazon Redshift, and other destinations. Along with Kinesis Data Streams, Kinesis Video Streams, and Amazon Kinesis Data Analytics, Kinesis Data Firehose is part of the Kinesis streaming data platform. The user does not need to create apps or manage resources while using Kinesis Data Firehose. Simply set up the data producers to transmit data to Kinesis Data Firehose, and the data will be sent to the designated destination automatically. The data can also be transformed before being delivered using Kinesis Data Firehose.  
