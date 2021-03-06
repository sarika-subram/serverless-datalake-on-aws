# Introduction to EC2, S3, and Datalake and Analytics on AWS

### Learning outcomes from this workshop
* Launching an EC2 instance
* Creation and various properties of S3
* Design serverless data lake architecture
* Build a data processing pipeline and Data Lake using Amazon S3 for storing data
* Use Amazon Kinesis for real-time streaming data
* Use AWS Glue to automatically catalog datasets
* Query data using Amazon Athena & visualize it using Amazon QuickSight
* Use Tensorflow on SageMaker

# Pre-requisites:  
* You need to have access to an AWS account with **AdminstratorAccess**
* This lab should be executed in **us-east-1** region
* Best is to **follow links from this  guide** & open them **in new a tab**
* Run this lab in a modern browser

# Syllabus

|Content| Link|
|:-----|:--:|
|Module 1: EC2 & S3 |[Open Lab :arrow_forward:](./Module1)|
|Module 2: Data Analytics |[Open Lab :arrow_forward:](./Module2)|
|Module 3: Tensorflow on SageMaker |[Open Lab :arrow_forward:](./Module3)|

# Clean Up

Failing to do this will result in incurring AWS usage charges.

Make sure you bring down/delete all resources created as part of this lab

## Resources to delete
* Kinesis Firehose Delivery Stream
	* GoTo: https://console.aws.amazon.com/firehose/home?region=us-east-1#/
	* Delete Firehose:  **aws-labseries-demo-stream**
* Glue Database
	* GoTo: https://console.aws.amazon.com/glue/home?region=us-east-1#catalog:tab=databases
	* Delete Database: **awslabs_db**
* Glue Crawler
	* GoTo: https://console.aws.amazon.com/glue/home?region=us-east-1#catalog:tab=crawlers
	* Delete Crawler: **CrawlDataFromKDG**
* Glue Dev Endpoint
	* GoTo: https://console.aws.amazon.com/glue/home?region=us-east-1#etl:tab=devEndpoints
	* Delete endpoint: **devendpoint1**
* Sagemaker Notebook
	* You may wish you download the notebook file locally on your laptop before deleting the notebook)
	* GoTo: https://console.aws.amazon.com/glue/home?region=us-east-1#etl:tab=notebooks
	* Delete Notebook: **aws-glue-notebook1**
* Delete IAM Role
	* GoTo: https://console.aws.amazon.com/iam/home?region=us-east-1#/roles
	* Search for AWSGlueServiceRoleLab
	* Delete Role: **AWSGlueServiceRoleLab**
* Delete S3 bucket
	* GoTo: https://s3.console.aws.amazon.com/s3/home?region=us-east-1
	* Delete Bucket: **YOUR_USERNAME-datalake-demo-bucket**
* Delete Cognito Setup :
	* Goto: https://us-west-2.console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/
	* Click: **Kinesis-Data-Generator-Cognito-User**
	* Click: **Actions** > **DeleteStack**
	* On confirmation screen: Click: **Delete**
* Close QuickSight account
	* GoTo: https://us-east-1.quicksight.aws.amazon.com/sn/admin#permissions
	* Click: **Unsubscribe**
* Cognito Userpool
	* GoTo: https://us-west-2.console.aws.amazon.com/cognito/users/?region=us-west-2#/

* [extra] VPC Endpoint: 
	* GoTo: https://console.aws.amazon.com/vpc/home?region=us-east-1#Endpoints:sort=vpcEndpointId

* [extra] RDS clusters: 
	* GoTo: https://console.aws.amazon.com/rds/home?region=us-east-1#databases:
	
* [extra] Elastic IPs: 
	* GoTo: https://us-east-2.console.aws.amazon.com/ec2/v2/home?region=us-east-2#SecurityGroups:sort=groupId
	
