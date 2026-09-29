# AWS Serverless Three-Tier Application

## Overview

Designed and implemented a lightweight, serverless three-tier web application using AWS managed services.

The application allows users to subscribe to monthly content through a web interface while leveraging a highly scalable and cost-effective cloud-native architecture.

## Architecture Diagram

<img width="807" height="436" alt="Serverless Architecture Diagram" src="https://github.com/user-attachments/assets/f2024046-c6c0-46ca-99a5-6fd04b62f6d5" />

## Business Problem

Traditional solutions often require dedicated servers, application hosting, and ongoing maintenance.

This project demonstrates how AWS managed services can provide a scalable, fault-tolerant, and cost-effective alternative.

## Architecture Components

### Presentation Tier

- Amazon S3
- Amazon CloudFront

Static website content is hosted in Amazon S3 and delivered through CloudFront.

### Logic Tier

- Amazon API Gateway
- Velocity Template Language (VTL)

API Gateway handles incoming requests and directly integrates with DynamoDB.

### Data Tier

- Amazon DynamoDB

DynamoDB stores subscription records and automatically scales based on demand.

## Key Design Decision

A major architectural decision was removing AWS Lambda from the solution.

Instead, API Gateway VTL mapping templates directly transform requests and write records into DynamoDB.

Benefits include:

- Lower latency
- Reduced costs
- Reduced operational overhead
- Fewer managed components

## AWS Services Used

- Amazon S3
- Amazon CloudFront
- Amazon API Gateway
- Amazon DynamoDB
- AWS IAM

## Screenshots

## Application Homepage

<img width="745" height="307" alt="homepage" src="https://github.com/user-attachments/assets/a4e3f875-8eba-43c8-b31f-49db2759a4a7" />
<img width="685" height="301" alt="subscription-successful" src="https://github.com/user-attachments/assets/4634b245-e06d-4e4c-8d9e-87a6e902c83b" />

## CloudFront Distribution

<img width="800" height="99" alt="CloudFront-Details" src="https://github.com/user-attachments/assets/1b7bfc74-70b0-433e-8994-a81fbbe0bb34" />

## API Gateway Integration

<img width="1603" height="770" alt="API-Gateway-Integration" src="https://github.com/user-attachments/assets/5ed27f49-cc3d-4b9d-86fc-950ec3538a5c" />

## S3 Bucket

<img width="799" height="160" alt="S3-bucket" src="https://github.com/user-attachments/assets/9f2c466c-b057-4a06-ab1e-547a40bacc20" />

## DynamoDB Records

<img width="803" height="375" alt="dynamodb-items" src="https://github.com/user-attachments/assets/ec1b8038-e044-4cd7-8be9-8a2166aa034b" />

## Author

Jonathan Machel

AWS Certified Solutions Architect - Associate
