# Automated AWS Receipt Processing System

### Overview of Project ☁️
This project focuses on automating receipt processing using AWS services. Instead of manually handling receipts which can be time-consuming, error-prone, and difficult to scale—this system extracts structured data from receipts and stores it efficiently for record-keeping and auditing.

### The architecture consists of:

* Storage Layer: Amazon S3 stores receipt images and PDFs.
* Processing Layer: Amazon Textract extracts text from receipts using AI-powered OCR.
* Database Layer: DynamoDB stores the extracted data in a structured format.
* Notification System: Amazon SES sends email alerts with receipt details.
* Compute Layer: AWS Lambda automates the workflow by processing the receipts in real-time.

### Services Used 🛠
* Amazon S3: Stores uploaded receipt images and PDFs. [Storage]
* Amazon Textract: Extracts text and structured data from scanned receipts.
* Amazon DynamoDB: Stores extracted receipt data in a structured format.
* Amazon SES: Sends email notifications with extracted receipt details.
* AWS Lambda: Automates the processing workflow for real-time execution. 
* IAM Roles & Policies: Ensures secure access between services.

### Architectural Diagram ✍️
<img width="1415" height="667" alt="image" src="https://github.com/user-attachments/assets/9338ab20-1969-42a6-9136-ad723e743ef6" />


### Steps to be performed ☁️
In this video, we'll be going through the following steps.

* Storage and Database Setup: S3 bucket and DynamoDB Table
* Notification Setup: Configuring Amazon SES
* Processing Setup: Creating a Lambda function
* Integration and Testing

### Clean Up 🗑️
1. Delete S3 Bucket: Remove all uploaded receipt files and then delete the bucket.
2. Stop Textract Processing: Ensure no further API calls are made to prevent extra costs.
3. Delete DynamoDB Table: Remove stored receipt data and then delete the table.
4. Disable SES Notifications: If SES was configured, remove verified email addresses.
5. Remove IAM Roles and Policies: Delete the IAM role created for the Lambda function.
