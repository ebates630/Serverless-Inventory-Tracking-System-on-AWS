# Serverless Inventory Tracking System on AWS

## What I Built
I built a fully serverless, event-driven inventory tracking system on AWS. It processes uploaded inventory files, stores inventory data, and sends notifications when items are out of stock — without managing servers.

## How It Works (Event Flow)
1) Upload inventory CSV to Amazon S3  
2) S3 triggers the Load-Inventory AWS Lambda function  
3) Lambda parses the CSV and writes items into Amazon DynamoDB  
4) DynamoDB Streams triggers the Check-Stock Lambda function  
5) If Count == 0, the function sends an alert through Amazon SNS  

## AWS Services Used
- Amazon S3
- AWS Lambda
- Amazon DynamoDB + DynamoDB Streams
- Amazon SNS
- AWS IAM

## Repo Structure
- src/lambdas/ -> Lambda function code
- src/sample-data/ -> sample CSV files
- src/scripts/ -> helper scripts
- docs/notes/ -> design notes and troubleshooting

## Author
Eric Bates
Data Analyst | AWS | Serverless | Event-Driven Architecture
