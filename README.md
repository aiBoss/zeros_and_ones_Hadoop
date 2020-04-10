# CSCI 5751_Hadoop_Impala_Project
> Ingest the sales data from the data warehouse into the data lake and prepare it for analysis and consumption.

### Group Name: zeros_and_ones

### Group Members: 
* Ayushi Rastogi,
* Krishna Shravya Gade
* Mourya Karan Reddy
* Roopana Vuppalapati Chenchu

## Table of contents
* [Description](#Description)
* [Technologies](#technologies)
* [Setup](#setupclouderavm)
* [Deployment Instructions](#deploymentnstructions)
* [Rollback script](#rollback script)

## Description
The data warehouse has data for Sales, Customers, Employees and Products. Given data has been cleaned, validated and stored in partitions to facilitate efficient analysis and visualization.
  ### Data Clean up & Validation
  The product has entries with price as zero. These entries have been removed since the price of a product cannot be 0?
  Few entries had price value with high precision (256.99999999...) These values have been rounded off to two decimals for an   easy visualization to users. 
  ### Data Partitions and Views
  * Views:
  <br /> customer_monthly_sales_2019_view and top_ten_customers_amount_view are created for a quick retrieval of monthy salesin 2019 and top 10 customers. Procedure to run these views is explained in the setup section. 
  * Partitions:
  <br /> 1. product_sales_partition: Total sales amount for each product is captured in this table and the data is partitioned on sales year and month
<br /> 2. customer_monthly_sales_2019_partitioned_view: This table gives monthly sales of each customer in 2019. The data partitioned on year and month. TODO Add time taken to run queries on partitioned and un part.. data
<br /> 3. product_region_sales_partition: Regional sales for each product is stored in this table and the data is partitioned on sales year and month

## Screenshots
![Example screenshot](./img/screenshot.png)

## Technologies
* VirtualBox Cloudera VM - version 5.13.0
  * HDFS
  * Impala

## Setup Cloudera VM
Follow the instructions in to install and configure Cloudera VM on local machine

## Deployment Instructions
* Download data from warehouse: https://csci5751-2020sp.s3-us-west-2.amazonaws.com/sales-data/salesda
ta.tar.gz
* Unzip the data
* Delete the zip file
* Load the raw data to HDFS
* Create an Impala data base with raw data: zeros_and_ones_sales_raw
* Create another data base with the clean data: zeros_and_ones_sales
* Create sales views 
  how to create ? we have to give run instructions or the sql files/ bash script (TODO)
* Create product_sales_partition
* Create partitioned
* Create product_region_sales_partition

## Rollback script
* Undo all the steps in one step  (TODO - script to undo)

