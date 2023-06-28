# Wells-Fargo-DataPlatform
## Business Case:
Wells Fargo has multiple internal applications that send huge amounts of data (petabytes) in CSV format daily in the company Azure cloud. We are required to perform data/schema validation on this incoming data and this needs to be stored in a delta table for downstream systems to make use for analysis.
<img width="784" alt="Screenshot 2023-06-27 at 7 54 52 PM" src="https://github.com/bluebarrete/Wells-Fargo_DataPipeline/assets/42550664/50ba1b31-b365-4fd5-be94-cc072e75a0fd">

            		    	       	               

## Task:

1. Validation needs to be applied as follows:

  1.1.	Need to check for duplicate rows. If file contains duplicate rows, it’s rejected.
  
  1.2.	Need to validate the data format for all the data fields, the date column names, and the date format is stored in the Azure            SQL server, if validation fails the file is rejected.
  
3.	Need to move all rejected files to Rejected folder.
   
5.	Need to move all valid files to Staging folder.
6.	Write all the validated files as a delta table in Azure Databricks

<img width="989" alt="highlevel arch" src="https://github.com/bluebarrete/Wells-Fargo_DataPipeline/assets/42550664/e18e7d6d-467d-465d-8270-9b9c9c8ff83b">


