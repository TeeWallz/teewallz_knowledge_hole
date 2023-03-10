# Data Engineering JargonDump

Source: [https://www.reddit.com/r/dataengineering/comments/rdw3b3/data_engineering_jargon/](https://www.reddit.com/r/dataengineering/comments/rdw3b3/data_engineering_jargon/)



## Data Dump
>A file or a table containing a significant amount of data to be analysed or transferred.
> 
>A table containing the "data dump" of all customer addresses.



## Data Pipelines
> A data processing method akin to a pipeline, which starts with data ingestion then processing then completion.
> 
> A pipeline where customer address data is ingested from source A and then aggregated according to their cities and this new information is loaded into destination B.

## DBA
> Database Administrator is an admin role that understands the particular database technology and how to get the best out of it. This includes improving performance, backups and recovery.
>
> Performance tuning the database to respond better to particular complex data queries.

## Data Warehouse
> A method of organising data to make it easy to analyse and report to make business decisions
> 
> Oracle data warehouse. Organising customer data in a data warehouse to be able to report the number of newly acquired customers.

## Data Mart
> A subset of a data warehouse, created for a very specific business use case.
> 
> Finance data mart storing all the relevant financial information required by the Accounting team to process their month-end cycles.

## ODS
> Operational data store generally stores limited and current information to help simple queries. Unable to handle historical or complex data queries.
> 
> An ODS for daily stock fluctuations in a warehouse help the warehouse manager decide what to prioritise in the next order delivery.

## EDW
> The same as a data warehouse except it includes all the data within an organisation. This means that the entire enterprise can rely on this warehouse for their business decisions.
> 
> Organising sales, customer, marketing and finance data in an enterprise data warehouse to be able to create several key management reports.

## RDBMS
> Relational database management system. All of the above examples are RDBMS, meaning they store data in a structured format using rows and columns.
> 
> A Microsoft SQL server database.

## In-memory DB

> Traditional databases have been used for complex calculations and queries. They store information on the actual disk in the computer. In-memory DB stores all the information on their memory (RAM), this allows for rapid calculations without read and write a function to a normal disk.
> 
> A drill-down functionality of a live dashboard.

## Data Lake
> A repository for all kinds of structured and unstructured data. Mainly based on Hadoop storage technology. Called a lake as it is flexible enough to store anything from raw data to unstructured email files.
>
> Hadoop Data Lake. Storing logs of all customers called into the inbound call centre including call duration.

## Ingestion
> Generally, the first step in a data pipeline, where data is inserted in tables in the platform.
>
> A pipeline where customer address data is inserted from source A.

## Extract, Transform, Load (ETL)
> A 3-step process of extracting data and transforming it (by applying some kind of logic like aggregation) and loading the new information into the destination. It could be used as ELT where the destination tables transform the data instead.
>
> An extract of customer address data is taken from the customer relationship management tool and is then aggregated according to their cities and this new information is loaded into destination B.

## Data Models
> A way of organising the data in a way that it can be understood in a real-world scenario.
>
> Taking a huge amount of data and logically grouping it into customer, product and location data.

## Normalisation
> A method of organising the data in a granular enough format that it can be utilised for different purposes over time. Usually, this is done by normalising the data into different forms such as 1NF (normal form) or 3NF (3rd normal form) which is the most common.
>
> Taking customer order data and creating granular information model; order in one table, item ordered in another table, customer contact in another table, payment of the order in another table. This allows for the data to be re-used for different purposes over time.

## Star schema
> The simplest way to model data into different quantitative and qualitative data is called facts and dimensions. Usually, the fact table is interpreted with the help of a dimensions table resembling a star.
>
> A Star schema of sales data with dimensions such as customer, product & time.

## Facts
> A data warehousing term for quantitative information.
>
> The number of orders placed by a customer.

## Dimensions
> A data warehousing term for qualitative information.
> 
> Name of the customer or their country of residence.

## Schemas
> A term for a collection of database objects. These are generally used to logically separate data within the database and apply access controls.
> 
> Storing HR data in HR schema allows logical segregation from other data in the organisation.

## SCD (slowly changing dimension) Type 1–6
> A method to deal with changes in the data over time in a data warehouse. Type 1 is when history is overwritten whereas Type 2 (most common) is when history is maintained each time a change occurs.
>
> When a customer changes their address; SCD Type 1 would overwrite the old address with the new one, whereas Type 2 would store both addresses to maintain history.

## Business Intelligence
> A slightly out of date term for a combination of practices to derive business insights from data by predominantly using data warehousing, analytics and dashboarding.
> 
> Creating a management dashboard to show customer demographics across the country.

## Batch Processing
> An automated way of processing millions of data transactions at the same time. This is  generally carried out overnight with the help of “batch jobs”.
> 
> Loading all the customer’s data that bought a particular item on the day.

## T-SQL
>SQL is a Structured Query Language or, simply put, a language used to manage databases. T-SQL is Transact-SQL which is a proprietary Microsoft extension of the SQL language.
>
>T-SQL can be used MS SQL Server or Azure SQL Database to write a statement as follows “SELECT customer_name from tbl_customer_information where customer_city = “London”. This provides the result of all the customer names where customers are based in London.

## NoSQL
>Although SQL has been around for decades, NoSQL (not only SQL) is a concept designed for non-relational databases, particularly to store unstructured data like documents.
>
>Storing an Outlook email file in XML with key-value pair on a MongoDB document database.

## BTEQ
>Batch Teradata Query (like SQL) is simply a utility and query tool for Teradata, which is a relational database system
>
>Creating a BTEQ script to load data from a flat file.

## Cloud
>Delivery of computing services such as servers, networking, analytics etc., over the internet instead of using a dedicated data centre for an organisation.
>
>Storing data on Microsoft’s Azure Cloud service instead of on an on-premise solution.

## Data Architecture
>The discipline of managing the people, processes and technologies relating to data; includes data strategy, data capture processes and technical patterns to derive insight from the data.
>
>A Data Architect creates a framework for an enterprise to manage its data flow end to end.

## Data Visualisation
>A practice for visualising large amounts of data to derive key insights to drive business decisions.
>
>An executive dashboard that clearly outlines the sales performance of a certain team.

## Data Centres
>A dedicated space (nowadays millions of sqft of space) which houses servers and systems for the organisation’s critical applications
>
>Microsoft Data Centre to host all the company’s critical applications.

## Data Integration
>Usually, the hardest part of the project, where multiple sources of data are integrated into a singular application/data warehouse.
>
>Integrating finance and customer relationship systems integrating into an MS SQL server database.

## Data Migration
>The practice of migrating the data from source to destination
>
>Migrating data from MS SQL server database to an Amazon Relational Database service

## Data Replication
>There are multiple ways to do this, but mainly it is a practice of copying data to multiple servers to protect an organisation against data loss.
>
>Replicating the customer information across two databases to ensure their core details are not lost.

## Big Data
>A term coined for large amounts of data that cannot be processed using traditional databases. Refer to Data Lake.
>
>EDIT: The 3 Vs that are defining properties of Big Data are Volume, Velocity & Variety.
>
>u/mrchowmein
>
>- thanks for the tip!
>
>Hadoop Data Lake stores all the information received from sensors in a smart fridge.

## Hive
>Apache Hive is a data warehouse open-source project that allows querying large amounts of data. Like SQL, it uses an easy-to-understand language called Hive QL.
>
>EDIT: Hive is the project that brought SQL querying capacities to Hadoop. An important point is that it's not a full database, because it doesn't manage the storage layer, but rather the combination of a query engine (turning SQL into map-reduce jobs) and a meta-store (table schemas, locations, statistics...) that allows querying existing data storage tools such as HDFS or other big data databases like HBase and many others.
>
>u/sib_n
>
>- thanks for additional information
>
>SELECT \ from tbl; returns all rows and columns from a data store like HDFS.*

## HDFS
>Hadoop Distributed File System is a data storage system used by Hadoop. It provides flexibility to manage structured or unstructured data.
>
>Storing large amounts of financial transactional data in an HDFS to query using Hive QL.

## NiFi
>It is an open-source extract, transform and load tool (refer to ETL); this allows filtering, integrating and joining data.
>
>Moving postcode data from a .csv file to HDFS using NiFi.

## Kafka
>It is more complex to work with than NiFi as it doesn’t have a user interface (UI), mainly used for real-time streaming data. It is a messaging system first created by LinkedIn engineers.
>
>Streaming real-time weather events using Kafka

## Flat File
>Flat files are commonly used to transfer data due to their basic nature; flat files are a single table storing data in a plain text format.
>
>EDIT: no nested fields which are common in other types of files such as XML and JSON (flat JSON-lines files are very common though). Nested structures are generally more disk-space efficient, but they are more complicated to parse and load elsewhere than flat files.
>
>u/sib_n
>
>- thanks for additional information
>
>All customer order numbers stored in a comma-separated value (.csv) file

## Latency
>The time it takes for a database or a web application to respond to a query or a click.
>
>Takes 30 seconds to query a database with 5 million records.

## Caching
>This is when limited data is stored on the RAM to allow for quick retrieval of information.
>
>In-memory caching of data in a database returns results to query 100 times faster.

## Staging
>The name of a storage area that is temporary in nature; to allow for processing of ETL jobs (refer to ETL).
>
>EDIT: Depending on the design of the ETL, this could be temporary or persistent but it is always an "intermediate" step rather than the final output table.
>
>A staging area in an ETL routine allows data to be cleaned before loading into the final tables.