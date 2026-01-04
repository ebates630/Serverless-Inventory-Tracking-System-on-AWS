# Serverless Inventory Tracking System on AWS

## Overview
This project implements a fully serverless, event-driven inventory tracking system on AWS. The goal was to eliminate server management, enable automatic scaling, and build a cost-efficient architecture that responds to events in real time.

The system processes uploaded inventory files, stores inventory data, and sends notifications when items are out of stock all using managed AWS services.

---

## Architecture Overview
- Inventory files are uploaded to Amazon S3  
- An S3 event triggers an AWS Lambda function to process and load data  
- Inventory data is stored in Amazon DynamoDB  
- DynamoDB Streams invoke a second Lambda function to evaluate inventory levels  
- When inventory reaches zero, alerts are sent using Amazon SNS  
- A serverless dashboard authenticates users with Amazon Cognito and reads data directly from DynamoDB  

**No EC2 instances. No capacity planning. Fully managed and auto-scaling.**

---

## What This Project Demonstrates
- Event-driven serverless architecture  
- Serverless compute using AWS Lambda  
- Loose coupling via S3 events and DynamoDB Streams  
- Scalable and reliable notification workflows  
- Pay-per-use, cost-optimized design  
- Clean separation of ingestion and business logic  

---

## AWS Services Used
- AWS Lambda  
- Amazon S3  
- Amazon DynamoDB  
- DynamoDB Streams  
- Amazon SNS  
- Amazon Cognito  
- AWS IAM  

---

## Future Enhancements
- Add Dead Letter Queues (DLQs) for Lambda error handling  
- Implement CloudWatch alarms and operational dashboards  
- Encrypt data using AWS KMS  
- Add Amazon API Gateway for real-time uploads  
- Enable AWS X-Ray for distributed tracing and observability  

---

## Author
Eric Bates  
Cloud & Data-Focused Professional | AWS | Serverless Architecture
