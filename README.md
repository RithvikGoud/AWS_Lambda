#Serverless Application for CSV Data Processing

## Project Overview
This project demonstrates how to create a serverless application on AWS that processes user-uploaded CSV files. The solution leverages AWS services such as **S3**, **Lambda**, and **DynamoDB** to implement a pipeline where:
1. User data in CSV format is uploaded to an S3 bucket.
2. A Lambda function is triggered to process the data, filtering the top 10 rows.
3. The processed data is stored in a DynamoDB table.
4. CloudWatch is used for monitoring and logging Lambda performance.

---

## Objectives
1. **Create an S3 bucket** for storing user-uploaded CSV files.
2. **Create a DynamoDB table** to store the processed data.
3. **Develop a Lambda function** to:
   - Process the CSV file by filtering the top 10 rows.
   - Store the filtered rows in DynamoDB.
4. Configure **event-driven triggers** for the Lambda function using S3.
5. Monitor and log performance using **CloudWatch**.

---

## Instructions

### AWS Setup
1. **S3 Bucket Creation**
   - Create an S3 bucket to store user-uploaded CSV files.
   - Configure appropriate permissions to allow Lambda access.

2. **DynamoDB Table Creation**
   - Create a DynamoDB table with the necessary schema to store processed CSV data.
   - Define the primary key (e.g., `RowID` or any unique identifier).

3. **Lambda Function Development**
   - Write a Lambda function in Python (or any supported language):
     - Parse the uploaded CSV file.
     - Filter the top 10 rows based on specific criteria.
     - Store the filtered rows into DynamoDB.
   - Deploy the Lambda function via AWS Management Console, AWS CLI, or Infrastructure as Code tools (e.g., AWS SAM, Terraform).

4. **Trigger Configuration**
   - Set up an S3 event notification to trigger the Lambda function whenever a new file is uploaded to the bucket.

5. **Monitoring with CloudWatch**
   - Enable CloudWatch logging for the Lambda function.
   - Use CloudWatch Metrics to monitor execution time, memory usage, and invocation count.

---

## How to Run

### AWS Workflow
1. **Upload CSV File**: Upload a CSV file to the S3 bucket.
2. **Trigger Lambda**: The Lambda function is automatically triggered by the S3 event.
3. **Process Data**: The Lambda function filters the top 10 rows and stores them in DynamoDB.
4. **Monitor Logs**: Use CloudWatch to view logs and performance metrics.

### Prerequisites
- AWS CLI or AWS Console access.
- IAM roles with permissions for S3, Lambda, DynamoDB, and CloudWatch.

---

## Tools and Technologies
- **AWS S3**: For file storage.
- **AWS Lambda**: For serverless processing.
- **AWS DynamoDB**: For storing processed data.
- **AWS CloudWatch**: For monitoring and logging.

